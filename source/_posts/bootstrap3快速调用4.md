---
title: bootstrap3快速调用4
date: 2018-09-11 17:47:10
tags: 
    - bootstrap
    - 输入框组
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
    <meta name="viewport" content="width=device-width, initial-scale=1, maximum-scale=1, user-scalable=no">
    <title>Document</title>
    <link rel="stylesheet" href="./bs/css/bootstrap.css">
    <script src='./bs/js/jquery.js'></script>
    <script src='./bs/js/bootstrap.js'></script>
    <style type="text/css">
        *{
            font-family: 微软雅黑;
        }
        .input-group{
            margin-top:15px;
        }
    </style>
</head>
<body>
<div class="container">
<h1 class="page-header">bootstrap</h1>
<form action="">
    <div class="input-group">
        <span class="input-group-addon">
            <input type='checkbox'>
        </span>
        <input type="text" class="form-control">
    </div>
    <div class="input-group">
        <span class="input-group-addon">$</span>
        <input type="text" class="form-control">
        <span class="input-group-addon">.00</span>
    </div>
    <div class="input-group">
        <span class="input-group-btn">
            <button class="btn btn-default">输入框组按钮</button>
        </span>
        <input type="text" class="form-control">
    </div>
    <div class="input-group">
        <div class="input-group-btn">
            <button class="btn btn-default" data-toggle='dropdown'>下拉菜单 <span class="caret"></span></button>
            <ul class="dropdown-menu">
                <li>1111111</li>
                <li>1111111</li>
                <li>1111111</li>
                <li>1111111</li>
            </ul>
        </div>
        <input type="text" class="form-control">
    </div>
    <div class="input-group">
        <span class="input-group-btn">
            <button class="btn btn-default">分列式下拉菜单</button>
            <button class="btn btn-default dropdown-toggle" data-toggle='dropdown'><span class="caret"></span></button>
            <ul class="dropdown-menu">
                <li>1111111</li>
                <li>1111111</li>
                <li>1111111</li>
                <li>1111111</li>
            </ul>
        </span>
        <input type="text" class='form-control'>
    </div>
    <div class="input-group">
        <span class="input-group-addon"><input type="checkbox" ></span>
        <input type="text" class="form-control">
        <span class="input-group-btn">
            <button class="btn btn-default">anniu</button>
            <button class="btn btn-default">anniu</button>
        </span>
    </div>
</form>
</div>
</body>
```
## [演示地址](http://www.guliansheng.club/bootstrap3/7.输入框组.html)
