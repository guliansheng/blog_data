---
title: javaScript基础2
date: 2018-09-10 21:04:21
tags: 
    - js基础
    - DOM基础
    - 元素属性设置
categories:
    - JavaScript基础
---
本篇是JavaScript基础第二节，主要介绍DOM的相关操作和元素属性值设置
>注：文中的[context]表示元素对象
<!-- more -->
## DOM元素

### 获取方法
- document.getElementById   (一个元素对象)

- [context].getElementsByTagName (元素集合)

- [context].getElementsByClassName (元素集合)

- document.getElementsByName  (节点集合[NodeList])

- document.documentElement (获取整个HTML对象)

- document.body  (获取整个BODY对象)

- document.head  (获取整个HEAD对象)

- [context].querySelector  (一个元素对象)

- [context].querySelectorAll  (获取元素集合)


### 元素节点
- 元素节点
    + nodeType：1 
    + nodeName：大写标签名（在部分浏览器的怪异模式下，我们写的标签名是小写，它获取的就是小写.…）
    + nodeValue：null
    + [curEle].tagName：获取当前元素的标签名（获取的标签名一般都是大写）

- 文本节点
    + nodeType：3 
    + nodeName：#text 
    + nodeValue：文本内容

- 注释节点
    + nodeType：8
    + nodeName：#comment
    + nodeValue：注释内容

- 文档节点
    + nodeType：9
    + nodeName：#document
    + nodeValue：null 


### 节点关系
- previousSibling：获取当前节点的上一个哥哥节点（不
一定是元素节点也可能是文本或者注释）

- nextSibling：获取当前节点的下一个弟弟节点

- firstChild：当前元素所有子节点中的第一个（也不一定是元素节点，可能是文本和注释）
- lastChild：当前元素所有子节点中的最后一个

- previousElementSibling：获取当前节点的上一个哥哥
元素节点

- nextElementSibling：获取当前节点的下一个弟弟元素节点

- firstElementChild  第一个子元素节点

- lastElementChild 最后一个子元素节点
> 获取[元素节点] (不是节点) 的方法都不兼容IE6~8;


### DOM渲染
- 回流(重排 reflow) ： 当页面中的HTML结构发生变化(增加，删除元素，位置发生变化...)，浏览器都需要重新计算一遍最新的DOM结构，重新对当前页面进行渲染

    > js中要尽量减少回流

- 重绘 ： 某一个元素的部分样式发生改变，浏览器只需要重新渲染当前元素即可

### DOM映射机制
 - 页面中的标签和js中获取到的元素对象(元素集合)是紧紧的绑定在一起的，页面中的HTML结构发生改变了，js中不需要重新获取，集合里面的内容也会跟着自动改变
```JavaScript
    var oUl=document.getElementById("ul");
    var oLis=oUl.getElementsByTagName("li");
    console.log(oLis.length);//->6
    var oLi=document.createElement("li");
    oUl.appendChild(oLi);
    console.log(oLis.length);//->7 没有重新的获取，但是oLis这个集合中的长度和内容会自动跟着发生改变
```

## 属性设置
### 设置自定义属性方法的区别
- xxx.index：是把当前操作的元素当做一个普通对象，为其设置一个属性名，和页面中的HTML标签没关系，不会在dom元素身上显示，但是可以在对象身上添加相应属性值

- xxx.setAttribute：把元素当做特殊的元素对象来处理，设置的自定义属性是和页面结构中的DOM元素映射在一起的，可以在HTML结构中看到设置的属性，但是没有在对象身上添加相应属性

### 自定属性和元素自带属性
- 与页面HTML结构无关的普通对象

- 与页面HTML结构存在映射关系的元素对象
    + 元素对象中的内置属性，大部分都和页面的标签存在映射关系
    
    + xxx.style.backgroundColor='xxx'此时不仅把JS中对象对应的属性值改变了，而且也会映射到页面的HTML标签上（标签中有一个style行内样式、元素的样式改变了）
    
    + xxx.className='xxx'此时不仅是把对象中的属性值改了，而且页面中的标签增加了class样式类（可以看见的）
