---
title: bootstrap3快速调用3
date: 2018-09-11 17:22:28
tags: 
    - bootstrap
    - 下拉菜单
    - 按钮组
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
        .dropdown-size{
            width: 100px;
            height: 40px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1 class="page-header">bootstrap</h1>
        <!-- 任何标签都可以做成下拉菜单 -->
        <div class="dropdown dropdown-size">
            <span data-toggle='dropdown'>xiala</span>
            <ul class="dropdown-menu">
                <li class="dropdown-header"><a href="">第一项</a></li>
                <li><a href="">1</a></li>
                <li><a href="">1</a></li>
                <li><a href="">1</a></li>
                <li class="divider"></li>
                <li class="dropdown-header">第二项</li>
                <li><a href="">2</a></li>
                <li><a href="">2</a></li>
                <li><a href="">2</a></li>
            </ul>
        </div>
        <br>
        <!-- 下拉菜单 -->
        <div class="row">
            <div class="dropdown col-sm-4 col-sm-offset-4">
              <button class="btn btn-default btn-lg" data-toggle="dropdown">
                Dropdown
                <span class="caret"></span><!-- 倒三角箭头，在下拉、上拉菜单中用该类，三角方向会自动改变 -->
              </button>
              <ul class="dropdown-menu" style="left: 15px">
                <li class="dropdown-header">第一项</li>
                <li><a href="#">Action</a></li>
                <li><a href="#">Another action</a></li>
                <li><a href="#">Something else here</a></li>
                <li class="divider"></li>
                <li class="dropdown-header">第二项</li>
                <li class="disabled"><a href="#">Separated link</a></li>
              </ul>
            </div>
        </div>
        <br>
        <!-- 上拉菜单 -->
        <div class="dropup">
            <button class="btn btn-info" data-toggle='dropdown'>上拉菜单<span class="caret"></span></button>
            <ul class="dropdown-menu">
                <li class="dropdown-header">第一项</li>
                <li><a href="#">Acti</a></li>
                <li><a href="#">Anoth</a></li>
                <li><a href="#">Somet</a></li>
                <li class="divider"></li>
                <li class="dropdown-header">第二项</li>
                <li><a href="#">Separa</a></li>
            </ul>
        </div>
        <br>
        <!-- 按钮式下拉菜单 -->
        <div class="btn-group">
            <button class="btn btn-info dropdown-toggle" data-toggle='dropdown'>单按钮下拉菜单<span class="caret"></span></button>
            <ul class="dropdown-menu">
                <li><a href="">1</a></li>
                <li><a href="">1</a></li>
                <li><a href="">1</a></li>
                <li><a href="">1</a></li>
            </ul>
        </div>
        <!-- 分裂式上拉菜单 -->
        <div class="btn-group dropup">
            <button class="btn btn-info">分列式下拉菜单</button>
            <button class="btn btn-info dropdown-toggle" data-toggle='dropdown'><span class="caret"></span></button>
            <ul class="dropdown-menu">
                <li><a href="">1</a></li>
                <li><a href="">1</a></li>
                <li><a href="">1</a></li>
                <li><a href="">1</a></li>
            </ul>
        </div>
        <br>
        <!-- 组合按钮 -->
        <div class="btn-group btn-group-justified">
            <div class="btn-group">
                <button class="btn btn-info">按钮</button>
            </div>
            <div class="btn-group">
                <button class="btn btn-info">按钮</button>
            </div>
            <div class="btn-group">
                <button class="btn btn-info">按钮</button>
            </div>
        </div>
        <br>
        <div class="btn-toolbar">
            <div class="btn-group btn-group-lg">
                <button class="btn btn-info">按钮</button>
                <button class="btn btn-info">按钮</button>
                <button class="btn btn-info">按钮</button>
            </div>
            <!-- 组合按钮下拉菜单 -->
            <div class="btn-group-vertical">
                <button class="btn btn-primary">按钮</button>
                <button class="btn btn-primary">按钮</button>
                <div class="btn-group">
                    <button class="btn btn-success dropdown-toggle" data-toggle='dropdown'>下拉菜单<span class="caret"></span></button>
                    <ul class="dropdown-menu">
                        <li class="dropdown-header"><a href="">第一项</a></li>
                        <li><a href="">1</a></li>
                        <li><a href="">1</a></li>
                        <li><a href="">1</a></li>
                        <li class="divider"></li>
                        <li class="dropdown-header">第二项</li>
                        <li><a href="">2</a></li>
                        <li><a href="">2</a></li>
                        <li><a href="">2</a></li>
                    </ul>
                </div>
            </div>
        </div>
    </div>
</body>

```

## [演示地址](http://www.guliansheng.club/bootstrap3/6.按钮组和下拉菜单.html)
