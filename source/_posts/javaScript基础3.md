---
title: javaScript基础3
date: 2018-09-10 21:07:06
tags: 
    - js基础
    - 正则表达式
categories:
    - JavaScript基础
---
本篇是JavaScript基础第三节，本章介绍正则的相关知识，详细介绍了正则的特性和应用
<!-- more -->
## 正则表达式

### 正则含义
- 他就是一个规则,用来处理字符串的一个规则(正则就是用来处理字符串)

### 创建正则
- 字面量方式: 
    - var reg = /\d/;
    
- 实例创建方式:
    - var reg = new RegExp("");

- 正则两种创建方式是有区别的
    - 在字面量方式中 , ‘//’之间包起来的所有 内容都是元字符,有的具有特殊的意义,大部分都是代表本身含义的普通元字符
    ```javaScript
    var name = 'gu'
    var reg = /^\d+"+name+"\d+$/;//并不是字符串拼接
    console.log(reg.test('200gu222')) //->flase
    console.log(reg.test('200'''guuu'222)) //->true

    //所以这种需求只能用实例方式创建
    
    var name = 'gu';
    reg = new RegExp("^\\d+"+name+"\\d+$","g");//这种方式创建时要注意转义字符
    console.log(reg.test('200gu222')) //->true;
    ```
    - 字面量中直接写\d就可以了,实例方式中需要转义 \\\d

### 处理字符串
- 匹配 : 使用reg.test(str)判断一个字符串是否符合我们制定的规则
```JavaScript
var reg = /\d/;
console.log(reg.test('zhu')); //->false
console.log(reg.test('1')); //->true
console.log(reg.test('zhufeng01')); //->true
```

- 捕获 : 使用reg.exec(str)把字符串中符合我们正则规则的内容捕获到
```JavaScript
var reg = /\d/;
console.log(reg.exec('zhu')); //->null
console.log(reg.exec('1')); //-> 1
```

- exec和match的区别

```javaScript
    var str2 = 'gu123gu234gu4560';
    var reg2 = /gu(\d+)/g;
    console.log(reg2.exec(str2)) //=>["gu123","123"...]
    console.log(reg2.exec(str2)) //=>["gu234","234"...]
    console.log(reg2.exec(str2)) //=>["gu345","345"...]
    console.log(str2.match(reg2)) //=>["gu123","gu234","gu345"]
```
    
### 正则捕获
- 每一次捕获的时候都是先进行默认匹配,如果没有匹配成功的,捕获的结果是null;只有有匹配的内容我们才能捕获到

- 捕获的内容:    
    - 捕获到的内容是一个数组
    
    - 数组中的第一项是当前正则捕获的内容
    
    - index : 捕获内容在字符串中开始的索引位置
    
    - input : 捕获的原始字符串

- 正则捕获特点:
    - 懒惰性 : 每一次执行exec只捕获第一匹配内容,在不进行任何处理的情况下,再次执行多次捕获,捕获内容还是第一匹配的内容
    
    > lastIndex : 是正则每一次捕获在字符串中开始查找的位置, 默认值是0, 如果不做任何处理, 每一次值都是0, 可以加全局修饰符 g 改变该值;
    
    - 贪婪性 : 正则每一次捕获都是按照匹配最长的结果捕获的, 符合正则条件时, 会完全捕获到
    
    > 解决贪婪性, 在量词元字符后面加上?元字符
    
    ```JavaScript
    var reg = /\d+?/g;
    var str = "29839jlsafi78789";
    //不加?结果:["29839"...]
    console.log(reg.exec(str));//=>["2"...]
    ```

    - 字符串方法match()可以直接获取到所有符合正则的内容, 不需要循环执行exec方法,但是match只能捕获大正则匹配的内容, 而对小正则捕获的内容是无法获取的(不能获取到分组的正则匹配)
    
### 正则分组
- 分组引用 
    ```JavaScript
    // \1代表和第一个分组一模一样的内容, \2代表和第二个分组一模一样的内容, 和对应的分组中的内容的值都要一样
    var reg = /^(\w)\1(\w)\2$/;
    console.log(reg.test("ffzz"));//true
    console.log(reg.test("fzz_"));//false
    ```

- 分组捕获 : 正则捕获的时候, 不仅仅把大正则匹配的内容捕获到, 而且还可以把小分组匹配的内容捕获到
    ```JavaScript
    // 在分组中使用 ?: 是只匹配不捕获
    var str = '342622199501013638';
    var reg=/^(\d{2})(\d{4})(\d{4})(\d{2})(\d{2})(\d{2})(\d)(?:\d|X)$/;
    console.log(reg.exec(str));// => ["342622199501013638", "34", "2622", "1995", "01", "01", "36", "3",  index: 0, input: "342622199501013638"]
    console.log(str.match(reg))//和上面效果相同

    var str2 = 'gu123gu234gu4560';
    var reg2 = /gu(\d+)/g;
    console.log(reg2.exec(str2)) //=>["gu123","123"...] 
    console.log(reg2.exec(str2)) //=>["gu234","234"...]
    console.log(reg2.exec(str2)) //=>["gu345","345"...]
    console.log(str2.match(reg2)) //=>["gu123","gu234","gu345"]
    ```

- replace执行机制
    ```JavaScript
    //和exec的机制相似
    var str = 'gu2893gu898gu674';
    var reg = /gu(\d+)/g;
    str.replace(reg,function(){ //捕获几次, 执行几次密名函数
        console.log(arguments) //arguments就是捕获到的值组成的类数组, 同样可以捕获到分组的内容
        return 'gu捕获到了' //return的值就是要替换的值
    })
    ```

## 常用正则

```JavaScript
    //1.有效数字正则：正数,负数,0,小数
    //-> "."可能出现, 可能不出现,出现后面必须跟一位或多位数字
    //-> 最开始可以有+/-也可以没有
    //-> 整数部分, 一位数也可以是0~9之间的一个, 多位数不能以0开头
    //
    //注意：
    //-> []中出现的所有字符只是自身字符的含义, 没有特殊含义
    var reg = /^[+-]?(\d|[1-9]\d+)(\.\d+)?$/


    //2.年龄在18~65
    //-> 18-19阶段
    //-> 20-59阶段
    //-> 60-65阶段
    //
    //注意：
    //-> []中不识别两位数
    //-> [12] 1或者2
    //-> [12-67] 1 , 2-6 , 7中的一个
    var reg = /^(1[8-9]|[2-5]\d|6[0-5])$/

    //3、验证邮箱的正则(简版)//左边：数字、字母、下环线、.、
    var reg=/^[\w.-]+@[0-9a-zA-Z]+(\.[a-zA-Z]{2,4}){1,2}$/;
    console.log(reg.test('1229303942@qq.com'))

    //4、中国标准真实姓名2-4位汉字
    var reg = /^[\u4e00-\u9fa5]{2,4}$/;
    console.log(reg.test('顾连生'))

    //5、身份证号码
    //var reg=/^\d{17}(\d|X)$/;
    //13 0828 1990 12 04 06 1 7
    var str = '342622194502047680';
    var reg=/^(\d{2})(\d{4})(\d{4})(\d{2})(\d{2})(\d{2})(\d)(\d|X)$/;
    console.log(reg.exec(str));
    console.log(str.match(reg));

```
