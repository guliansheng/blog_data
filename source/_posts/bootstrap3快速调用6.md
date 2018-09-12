---
title: bootstrap3快速调用6
date: 2018-09-11 17:57:41
tags: 
    - bootstrap
    - 导航条
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
        *{
            font-family: 微软雅黑;
        }
        body{
            margin-top:30px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1 class="page-header">bootstrap</h1>
        <!-- 固定导航条在顶部navbar-fixed-top;导航条固定在底部navbar-fixed-bottom；导航条背景可自行设置，有两种通用类，navbar-default和navbar-inverse(反色) -->
        <nav class="navbar navbar-default  navbar-fixed-top" >
        <div class="container">
            <div class="navbar-header">
                <!-- 主题部分可以是文字也可以是logo -->
                <a href="" class="navbar-brand"><img src="./image/logo.png" height="130%" alt=""></a>
                <!-- 合并区展开按钮，用于小屏幕； -->
                <button class="navbar-toggle collapsed" data-toggle='collapse' data-target='#mynavbar'>
                    <span class="icon-bar"></span>
                    <span class="icon-bar"></span>
                    <span class="icon-bar"></span>
                </button>
            </div>
            <!-- 合并区内容放在mynavbar中； -->
            <div id="mynavbar" class="collapse navbar-collapse">
                <ul class="nav navbar-nav">
                    <li><a href="#">起步</a></li>
                    <li><a href="">全局css样式</a></li>
                    <!-- 插入按钮 -->
                    <li><button class="btn btn-default navbar-btn btn-sm">查询</button></li>
                    <!-- 插入表单 -->
                    <form class="navbar-form navbar-left">
                        <div class="form-group">
                        <input type="text" class="form-control input-sm" placeholder="Search">
                        </div>
                        <button type="submit" class="btn btn-default btn-sm "><span class="glyphicon glyphicon-search"></span></button>
                    </form>
                    <!-- 添加文字和链接 -->
                    <p class="navbar-text">bootstrap <a href="" class="navbar-link">链接</a></p>
                </ul>
                <ul class="nav navbar-nav navbar-right">
                    <!-- 添加下拉菜单 -->
                    <li class="dropdown">
                        <a href="" class="dropdown-toggle" data-toggle='dropdown'><span>bootstrap中文网</span> <span class="caret"></span></a>
                        <ul class="dropdown-menu">
                            <li class=".dropdown-header"><a href="">bootstrap</a></li>
                            <li><a href="">bootstrap</a></li>
                            <li class="divider"></li>
                            <li><a href="">bootstrap</a></li>
                            <li><a href="">bootstrap</a></li>
                        </ul>
                    </li>
                </ul>
            </div>
        </div>
        </nav>
        <!-- 路径导航 -->
        <ol class="breadcrumb">
            <li><a href="">bootstrap</a></li>
            <li><a href="">bootstrap</a></li>
            <li><a href="">bootstrap</a></li>
            <li><a href="">bootstrap</a></li>
            <li class="active">bootstrap</li>
        </ol>
        <h3>0001</h3>
        <h3>0002</h3>
        <h3>0003</h3>
        <h3>0004</h3>
        <h3>0005</h3>
        <h3>0006</h3>
        <h3>0007</h3>
        <h3>0008</h3>
        <h3>0009</h3>
        <h3>0010</h3>
        <h3>0011</h3>
        <h3>0012</h3>
        <h3>0013</h3>
        <h3>0014</h3>
        <h3>0015</h3>
        <h3>0016</h3>
        <h3>0017</h3>
        <h3>0018</h3>
        <h3>0019</h3>
        <h3>0020</h3>
        <h3>0021</h3>
        <h3>0022</h3>
        <h3>0023</h3>
        <h3>0024</h3>
    </div>
</body>
<script>
$('.navbar-nav li').mouseenter(function(){
    $(this).addClass('active');
    $('.navbar-nav li').not($(this)).removeClass('active');
})
</script>
</html>

```
## [演示地址](http://www.guliansheng.club/bootstrap3/9.导航条.html)
