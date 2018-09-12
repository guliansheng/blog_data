---
title: bootstrap3快速调用11
date: 2018-09-11 23:00:44
tags:
    - 工具提示
    - 弹框
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
    .MYcarousel{
        width: 1000px;
        height: 400px;
        margin: 0 auto;
    }
    .carousel-caption{
        width: 1000px;
        height: 100px;
        background: #000;
        opacity: 0.7;
        position: absolute;
        left: 0!important;
        bottom: 50px!important;
    }
    .carousel-caption h3{
        margin: 0;
    }
    </style>
</head>
<body>
        <h1 class="page-header">幻灯片</h1>
        <div class="MYcarousel">
        <div id="mycarousel" class="carousel slide" data-ride="carousel" >
            <!-- 幻灯片 -->
            <div class="carousel-inner" role="listbox">
                <div class="item active">
                    <img src="./image/1.jpg" width='100%'  alt="...">
                    <div class="carousel-caption">
                        <h3>第一张</h3>
                        <p>幻灯片图片解释</p>
                    </div>
                </div>
                <div class="item">
                    <img src="./image/2.jpg" width='100%'  alt="...">
                    <div class="carousel-caption">
                        <h3>第二张</h3>
                        <p>幻灯片图片解释</p>
                    </div>
                </div>
                <div class="item">
                    <img src="./image/3.jpg" width='100%'  alt="...">
                    <div class="carousel-caption">
                        <h3>第三张</h3>
                        <p>幻灯片图片解释</p>
                    </div>
                </div>
            </div>
            <!-- 指示灯 -->
            <ol class="carousel-indicators">
                <li data-target="#mycarousel" data-slide-to="0" class="active"></li>
                <li data-target="#mycarousel" data-slide-to="1"></li>
                <li data-target="#mycarousel" data-slide-to="2"></li>
            </ol>
            <!-- 左右控制 -->
            <a class="left carousel-control" href="#mycarousel" data-slide="prev">
                <span class="glyphicon glyphicon-chevron-left"></span><!-- 左图标 -->
                <span class="sr-only">Previous</span>
            </a>
            <a class="right carousel-control" href="#mycarousel" data-slide="next">
                <span class="glyphicon glyphicon-chevron-right"></span><!-- 右图标 -->
                <span class="sr-only">Next</span>
            </a>
        </div>
        </div>
</body>
</html>

```
## [演示地址](http://www.guliansheng.club/bootstrap3/15.幻灯片.html)


