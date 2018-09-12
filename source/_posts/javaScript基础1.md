---
title: javaScript基础1
date: 2018-09-10 20:24:00
tags: 
    - js基础
    - 控制台
categories:
    - JavaScript基础
---
本篇是JavaScript基础第一节，主要是查漏一些基础内容和平时可能不注意的地方, 有问题可在下方留言
<!-- more -->
## 基础

### 弹出框
- 弹出框的内容最后都会被转换为字符串输出(调用toString这个方法)
```javascript
    alert(1 + 1);//=>"2";
```

### 控制台
- console.dir()：比console.log()更加详细
- console.table()：将json以表格形式展现出来

### 命名规范
- 常用简写
    - info：information 信息
    - init：initialization 初始化
    - add / insert / create：增加/创建/插入
    - remove / rm / clear / del / delete：删除
    - get / query / select：查询/获取
- 常规规范
    - var _XXX：一般以下划线开头的代表变量是一个全局或者公用的变量
    - JS中很多的词都是有特殊含义的，我们这些词叫做关键字；现在没有特殊含义，以后可能会作为关键词的，我们叫做保留字；而关键字和保留字都不可以随便用来命名

### 数据类型转换
- '==' 两边
    + 两个等于号比较，左右两边数据值的类型不一样，浏览器会把两边的类型使用Number()方法都转换为数字然后再比较，但是null和undefined除外
    ```JavaScript
    null == undefined  //=> true
    null === undefined //=> false 
    null == 0 //=>false  null和undefined和其他任何值都不相等

    ```
    + 等号两边类型相同,进行 '===' 比较

### Math
- random 获取[n,m]之间的随机整数

```JavaScript
Math.round(Math.random()*(m-n)+n)
```

### 括号表达式

```JavaScript
    function fn1() {
        console.log(this);
    }
    function fn2() {
        console.log(this);
    }
    var json = {name:'gu',fn:fn2};
    ;(fn1,fn2)() //括号表达式中每一项用","隔开，最后只能获取到最后一项
    ;(fn1,json.fn)() //这里只是将json.fn指向的fn2函数直接拿过来使用，所以this还是指向window
    ;(json.fn)() //只有一项时，this还是指向json
```

