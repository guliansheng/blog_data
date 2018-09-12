---
title: bootstrap3快速调用8
date: 2018-09-11 19:09:24
tags: 
    - bootstrap
    - 列表组
    - 面板
    - 列表组和面板
    - 表格和面板
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
    <link rel="stylesheet" type="text/css" href="./bs/css/bootstrap.css">
    <script type="text/javascript" src='./bs/js/jquery.js'></script>
    <script type="text/javascript" src='./bs/js/bootstrap.js'></script>
</head>
<body>
<div class="container">
<h1>列表组 <small><mark>一般用于消息展示</mark></small></h1>
<hr>
<div class="row">
<div class="col-md-6">
<div class="list-group">
            <a href="#" class="list-group-item active">
                <h4 class="list-group-item-heading">List group item heading</h4>
                <p class="list-group-item-text">List group item headingList group item headingList group item headingList group item headingList group item headingList group item headingList group item headingList group item headingList group</p>
            </a>
            <a href="#" class="list-group-item">
                <h4 class="list-group-item-heading">List group item heading</h4>
                <p class="list-group-item-text">List group item headingList group item headingList group item headingList group item headingList group item headingList group item headingList group item headingList group item headingList</p>
            </a>
            <a href="#" class="list-group-item ">
                <h4 class="list-group-item-heading">List group item heading</h4>
                <p class="list-group-item-text">List group item headingList group item headingList group item headingList group item headingList group item headingList group item headingList group item headingList group item headingList</p>
            </a>
</div>
</div>
<div class="col-md-6">
    <div class="list-group">
        <a href="#" class="list-group-item active">
            <h4 class="list-group-item-heading">List group item heading</h4>
            <p class="list-group-item-text">List group item headingList group item headingList group item headingList group item headingList group item headingList group item headingList group item headingList group item headingList group</p>
        </a>
        <a href="#" class="list-group-item">
            <h4 class="list-group-item-heading">List group item heading</h4>
            <p class="list-group-item-text">List group item headingList group item headingList group item headingList group item headingList group item headingList group item headingList group item headingList group item headingList</p>
        </a>
        <a href="#" class="list-group-item ">
            <h4 class="list-group-item-heading">List group item heading</h4>
            <p class="list-group-item-text">List group item headingList group item headingList group item headingList group item headingList group item headingList group item headingList group item headingList group item headingList</p>
        </a>
    </div>
</div>
</div>
<h1>面板 <small><mark>新闻展示，公告展示</mark></small></h1><!-- 面板效果 -->
<hr>
<div class="panel panel-primary">
    <div class="panel-heading">
        <div class="panel-titel">
            <h2>面板效果</h2>
        </div>
    </div>
    <div class="panel-body">
        <h4>linux</h4>
    </div>
    <div class="panel-footer">
        <p>linux is very much!linux is very much!linux is very much!linux is very much!linux is very much!linux is very much!linux is very much!linux is very much!linux is very much!</p>
    </div>
</div>
<h1>面板和列表组 <small><mark>新闻展示，公告展示</mark></small></h1><!-- 面板列表组效果：一般不用加body和footer直接加入列表组 -->
<hr>
<div class="row">
    <div class="col-md-6">
        <div class="panel panel-primary">
            <div class="panel-heading">
                <div class="panel-titel">
                    <h2>面板加列表组效果</h2>
                </div>
            </div>
            <div class="panel-body">
                <div class="list-group">
            <a href="#" class="list-group-item ">
                <h4 class="list-group-item-heading">List group item heading</h4>
                <p class="list-group-item-text">List group item headingList group item headingList group item headingList group item headingList group item headingList group item headingList group item headingList group item headingList group</p>
            </a>
            <a href="#" class="list-group-item">
                <h4 class="list-group-item-heading">List group item heading</h4>
                <p class="list-group-item-text">List group item headingList group item headingList group item headingList group item headingList group item headingList group item headingList group item headingList group item headingList</p>
            </a>
            <a href="#" class="list-group-item ">
                <h4 class="list-group-item-heading">List group item heading</h4>
                <p class="list-group-item-text">List group item headingList group item headingList group item headingList group item headingList group item headingList group item headingList group item headingList group item headingList</p>
            </a>
            </div>
            </div>
            <!-- <div class="panel-footer">
                <p>linux is very much!linux is very much!linux is very much!linux is very much!linux is very much!linux is very much!linux is very much!linux is very much!linux is very much!</p>
            </div> -->
        </div>
    </div>
    <div class="col-md-6">
        <div class="panel panel-info">
            <div class="panel-heading">
                <div class="panel-titel">
                    <h2>面板加列表组效果</h2>
                </div>
            </div>
            <!-- <div class="panel-body"> -->
                <div class="list-group">
            <a href="#" class="list-group-item ">
                <h4 class="list-group-item-heading">List group item heading</h4>
                <p class="list-group-item-text">List group item headingList group item headingList group item headingList group item headingList group item headingList group item headingList group item headingList group item headingList group</p>
            </a>
            <a href="#" class="list-group-item">
                <h4 class="list-group-item-heading">List group item heading</h4>
                <p class="list-group-item-text">List group item headingList group item headingList group item headingList group item headingList group item headingList group item headingList group item headingList group item headingList</p>
            </a>
            <a href="#" class="list-group-item ">
                <h4 class="list-group-item-heading">List group item heading</h4>
                <p class="list-group-item-text">List group item headingList group item headingList group item headingList group item headingList group item headingList group item headingList group item headingList group item headingList</p>
            </a>
            </div>
            <!-- </div> -->
            <div class="panel-footer">
                <p>linux is very much!linux is very much!linux is very much!linux is very </p>
            </div>
        </div>
    </div>
</div>
<h1>面板加入表格</h1><!-- 面板中加入表格和加入列表相似 -->
<hr>
<div class="panel panel-primary">
    <div class="panel-heading">
        <div class="panel-titel">
            <h4>面板表格效果</h4>
        </div>
    </div>
    <table class="table table-striped table-hover table-bordered">
        <tr>
            <th>id</th>
            <th>username</th>
            <th>password</th>
        </tr>
        <tr>
            <td>001</td>
            <td>002</td>
            <td>003</td>
        </tr>
        <tr>
            <td>001</td>
            <td>002</td>
            <td>003</td>
        </tr>
        <tr>
            <td>001</td>
            <td>002</td>
            <td>003</td>
        </tr>
        <tr>
            <td>001</td>
            <td>002</td>
            <td>003</td>
        </tr>
        <tr>
            <td>001</td>
            <td>002</td>
            <td>003</td>
        </tr>
    </table>
    <div class="panel-footer">
        <p><mark>下方可加入说明文字等</mark></p>
    </div>
</div>
</div>
</body>
</html>

```
## [演示地址](http://www.guliansheng.club/bootstrap3/11.列表组和面板.html)

