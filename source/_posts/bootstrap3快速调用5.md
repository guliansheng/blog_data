---
title: bootstrap3快速调用5
date: 2018-09-11 17:51:25
tags: 
    - bootstrap
    - 菜单栏
categories:
    - bootstrap3快速调用
---
本篇章需要有一定的bootstrap基础，这里主要是将一些常用的功能集合起来，方便直接调用，并且相关代码已经经过处理可以直接使用，不需要额外调试，如发现问题可先查看是否为版本问题，如不是可在下方给我留言，我会及时作出回复（评论系统较慢，望谅解），文中有关的css，js文件的引用需要自行配置，如需要完整版可前往我的 <font size="4">[github](https://github.com/guliansheng/bootstrap3)</font> 仓库下载源码
<!-- more -->
## 源码
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <link rel="stylesheet" href="./bs/css/bootstrap.css">
    <script src='./bs/js/jquery.js'></script>
    <script src='./bs/js/bootstrap.js'></script>
    <style type="text/css">
        .daohang1{
            margin: 15px 15px;
        }
        a{
            cursor: pointer;
        }
    </style>
</head>
<body>
<div class="container">
    <h1 class="page-header">bootstrap</h1>
    <ul class="nav nav-tabs">
        <li class="active"><a>menu1</a></li>
        <li><a>menu2</a></li>
        <li class="dropdown"><a class="dropdown-toggle" data-toggle='dropdown'>menu3 <span class="caret"></span></a>
            <ul class="dropdown-menu">
                <li><a href="">1</a></li>
                <li><a href="">1</a></li>
                <li><a href="">1</a></li>
                <li><a href="">1</a></li>
            </ul>
        </li>
    </ul>
    <div class="daohang1">
        <p class="lead">i like bootstrapi like bootstrapi like bootstrapi like bootstrapi like bootstrapi like bootstrapi like bootstrapi like bootstrapi like bootstrapi like bootstrap i like bootstrapi like bootstrapi like bootstrapi like bootstrapi like bootstrapi like bootstrapi like bootstrapi like bootstrapi like bootstrapi like bootstrap</p>
        <p class="lead">i like jsi like jsi like jsi like jsi like jsi like jsi like jsi like jsi like jsi like jsi like jsi like jsi like jsi like jsi like jsi like jsi like jsi like jsi like jsi like jsi like jsi like jsi like jsi like jsi like jsi like jsi like jsi like jsi like jsi like jsi like jsi like jsi like jsi like jsi like jsi like jsi like jsi like jsi like jsi like jsi like jsi like js</p>
        <p class="lead">i like bsi like bsi like bsi like bsi like bsi like bsi like bsi like bsi like bsi like bsi like bsi like bsi like bsi like bsi like bsi like bsi like bsi like bsi like bsi like bsi like bsi like bsi like bsi like bsi like bsi like bsi like bsi like bsi like bsi like bsi like bsi like bsi like bsi like bsi like bsi like bsi like bsi like bsi like bsi like bsi like bsi like bs</p>
    </div>
    <ul class="nav nav-pills">
        <li class="active"><a href="">menu1</a></li>
        <li><a href="">menu2</a></li>
        <li class="dropdown"><a href="" class="dropdown-toggle" data-toggle='dropdown'>menu3 <span class="caret"></span></a>
            <ul class="dropdown-menu">
                <li><a href="">1</a></li>
                <li><a href="">1</a></li>
                <li><a href="">1</a></li>
                <li><a href="">1</a></li>
            </ul>
        </li>
    </ul>
    <ul class="nav nav-pills nav-stacked col-md-3">
        <li class="active"><a href="">menu1</a></li>
        <li><a href="">menu2</a></li>
        <li class="dropdown"><a href="" class="dropdown-toggle" data-toggle='dropdown'>menu3 <span class="caret"></span></a>
            <ul class="dropdown-menu">
                <li><a href="">1</a></li>
                <li><a href="">1</a></li>
                <li><a href="">1</a></li>
                <li><a href="">1</a></li>
            </ul>
        </li>
    </ul>
    <div class="daohang2 col-md-9">
        <p class="lead">i like bootstrapi like bootstrapi like bootstrapi like bootstrapi like bootstrapi like bootstrapi like bootstrapi like bootstrapi like bootstrapi like bootstrap i like bootstrapi like bootstrapi like bootstrapi like bootstrapi like bootstrapi like bootstrapi like bootstrapi like bootstrapi like bootstrapi like bootstrap</p>
        <p class="lead">i like jsi like jsi like jsi like jsi like jsi like jsi like jsi like jsi like jsi like jsi like jsi like jsi like jsi like jsi like jsi like jsi like jsi like jsi like jsi like jsi like jsi like jsi like jsi like jsi like jsi like jsi like jsi like jsi like jsi like jsi like jsi like jsi like jsi like jsi like jsi like jsi like jsi like jsi like jsi like jsi like jsi like js</p>
        <p class="lead">i like bsi like bsi like bsi like bsi like bsi like bsi like bsi like bsi like bsi like bsi like bsi like bsi like bsi like bsi like bsi like bsi like bsi like bsi like bsi like bsi like bsi like bsi like bsi like bsi like bsi like bsi like bsi like bsi like bsi like bsi like bsi like bsi like bsi like bsi like bsi like bsi like bsi like bsi like bsi like bsi like bsi like bs</p>
    </div>
</div>
</body>
<script>
    $('.daohang1 p').not($('.daohang1 p').eq(0)).stop().hide(100);
    $('.nav-tabs li').click(function(){
        $(this).addClass('active');
        $('.nav-tabs li').not($(this)).removeClass('active');
        ind=$(this).index('.nav-tabs li');
        $('.daohang1 p').eq(ind).stop().show(100);
        $('.daohang1 p').not($('.daohang1 p').eq(ind)).stop().hide(100);
    });
    $('.daohang2 p').not($('.daohang2 p').eq(0)).stop().hide(100);
    $('.nav-pills li').mouseenter(function(){
        $(this).addClass('active');
        $('.nav-pills li').not($(this)).removeClass('active');
        ind=$(this).index('.nav-pills li');
        $('.daohang2 p').eq(ind).stop().show(100);
        $('.daohang2 p').not($('.daohang2 p').eq(ind)).stop().hide(100);
    });
</script>
</html>

```
## [演示地址](http://www.guliansheng.club/bootstrap3/8.导航.html)
