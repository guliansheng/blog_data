---
title: javaScript基础4
date: 2018-09-10 21:24:34
tags: 
    - js基础
    - 事件基础
    - 二级事件绑定
categories:
    - JavaScript基础
---
本篇是JavaScript基础第四节，这是js基础的最后一个篇章，主要讲述事件的基础以及事件的传播机制，DOM二级事件绑定
>文中出现的html代码样式请自行设置
<!-- more -->
## 事件
### 非常用事件
- onmousewheel (鼠标滚轮滚动行为)

- onresize (window.onresize浏览器窗口大小改变事件)

- onunload (浏览器关闭事件)

### 鼠标事件
- 原型链: MouseEvent --> UIEevent --> Event --> Object

- MouseEvent 记录的是页面中唯一一个鼠标每一次触发时候的相关信息,和到底在哪个元素上触发的没有关系

- pageX | Y兼容处理 : event.pageX | Y = event.pageX | Y || (e.clientX + (document.documentElement.scrollLeft | Top || document.body.scrollLeft | Top));

### 事件传播机制
- 先进行捕获阶段,再到目标阶段(可以不加),最后是冒泡阶段

- 使用DOM零级事件给元素的某一个行为绑定的方法,都是在行为触发后的冒泡阶段把方法执行的

- 无论元素是否绑定行为方法,都会触发相关事件,并进行事件传播,只是不绑定方法的不会有方法被执行
- 
![Image 事件传播机制（图片来源：珠峰培训）](http://www.guliansheng.club/img/blog/js/事件传播机制.jpg)

### 事件监听
```html
<body>
    <div class="box1">
        <div class="box2">
            <div class="box3"></div>
        </div>
    </div>
</body>
<script>
    let box1=document.querySelector('.box1');
    let box2=document.querySelector('.box2');
    let box3=document.querySelector('.box3');
    var Event = {
        addEvent: function(element,type,callback){
            if(element.addEventListener){
                element.addEventListener(type,callback,false);
            }else if(element.attachEvent){
                element.attachEvent('on' + type,callback);//只在冒泡阶段发生,ie6~8兼容,也可以在ie9+使用
            }
        },
        removeEvent: function(element,type,callback){
            if(element.removeEventListener){
                element.removeEventListener(type,callback,false);
            }else{
                element.detachEvent('on' + type, callback);
            }
        },
        getEvent: function(event){
            event = event || window.event;
            return event;
        },
        getTarget: function(event){
            if(window.event){event=window.event}
            return event.target || event.srcElement;
        },
        stopPropagation: function(event){
            if(window.event){event=window.event}
            if(event.stopPropagation){
                event.stopPropagation();
            }else{
                event.cancelBubble = true;
            }
        },
        preventDefault: function(event){
            if(window.event){event=window.event}//兼容ie获取事件对象；
            if(event.prevenDefault){
                event.preventDefault();
            }else{
                event.returnValue = false;
            }
        }
    }
    Event.addEvent(box3,'click',function click(event){
        alert(box3.className);
        console.log(Event.getEvent(event.target));
        //参数:元素对象 , 移除的行为 , 移除的绑定方法名
        Event.removeEvent(box3,'click',click);
    });

    Event.addEvent(box2,'click',function click(event){
        alert(box2.className);
        console.log(event);
        console.log(Event.getEvent(event.type));
        Event.removeEvent(box2,'click',click);
    });
    Event.addEvent(box1,'click',function click(event){
        alert(box1.className);
        console.log(Event.getEvent(event.target));
        Event.removeEvent(box3,'click',click);
    });
</script>
```

### 事件委托
```html
<body>
    <ul id="list">
        <li id="item1" >item1</li>
        <li id="item2" >item2</li>
        <li id="item3" >item3</li>
    </ul>
</body>
<script>
    //利用事件的冒泡机制(触发当前元素的某个行为,他父级所有元素的相关行为都会触发),如果一个容器中有很多元素都绑定点击事件,我们没必要一个个的绑定了,只需要给最外层容器绑定一个点击事件即可,在这个方法执行的时候,通过事件源的区分来进行不同的操作;
    var list = document.getElementById("list");
    document.addEventListener("click",function(event){
        var target = event.target;//event.target返回触发该事件的元素；
        if(target.tagName == "LI"){//当元素为li标签时（tagName和nodeName都可以）
            //TODO
            alert(target.innerHTML);
        }
    })
    var node=document.createElement("li");
    node.innerHTML='这还少';
    list.appendChild(node);
</script>
```

## DOM二级事件绑定
### 原理
- 是让元素对象通过原型链一直找到EventTarget这个内置类原型上的addEventListener方法实现的

### 二级事件绑定和零级事件绑定的区别
- DOM零级事件绑定 : 只能给一个元素的某个行为绑定一次方法, 第二次绑定会把之前的覆盖掉

- DOM二级事件绑定 : 可以给某个元素同一个行为绑定多个 "不同" 的方法 , 如果方法相同只能留一个 , 但是在捕获和冒泡阶段可以为同一个行为绑定同一个方法,因为是在不同阶段执行的

- DOM零中的事件类型都可以绑定 , 并且DOM二级中提供了一些DOM零级没有的行为类型 (DOMContentLoaded : 当页面中的DOM结构[html结构]加载完成时触发的行为)
    
    - window.onload = function(){} -> 当页面中的所有资源加载完成(图片 , HTML结构 , 音视频 ...)才会执行后面的函数;并且同一个页面中只能用一次 , 后面再写会把前面的覆盖掉; => 因为他是采用DOM零级事件绑定的
    
    - jQuery: \$(document).ready(function(){}) -> $(function(){}) 只要当前页面中的HTML结构加载完成就会执行对应的函数;并且同一个页面中可以出现多次;这是因为他采用DOM二级事件绑定 , 并且绑定的行为是DOM二级中新增的DOMContentLoaded

### 绑定和移除
- 绑定: el.addEventListener('行为' , 方法名 , 传播方式);

- 移除: el.removeEventListener('行为' , 方法名 , 传播方式);

### 执行过程
- 可以给某个元素同一个行为绑定多个 "不同" 的方法 , 如果方法相同只能留一个 , 但是在捕获和冒泡阶段可以为同一个行为绑定同一个方法,因为是在不同阶段执行的

- 当行为触发 , 会按照绑定的先后顺序依次把绑定的方法执行

- 执行的方法中的this就是当前被绑定事件的元素本身

### ie6~8兼容问题
- 顺序问题：执行的时候顺序是混乱的，标淮浏览器是按照绑定顺序依次执行的

- 重复问题：IE6～8可以给同一个元素的同一个行为绑定多个相同的方法

- this问题：IE6～8中当方法执行的时候，方法中的this不是当前绑定的元素而是window
