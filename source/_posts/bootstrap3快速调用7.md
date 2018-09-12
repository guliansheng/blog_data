---
title: bootstrap3快速调用7
date: 2018-09-11 19:00:12
tags: 
    - bootstrap
    - 分页
    - 进度条
    - 自定义展示（常用）
    - 关闭按钮
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
    <script src='./bs/js/docs.js'></script>
    <script src='./bs/js/jquery.js'></script>
    <script src='./bs/js/bootstrap.js'></script>

    <style type="text/css">
        *{
            font-family: 微软雅黑;
        }
    </style>
</head>
<body>
<div class="container">

    <h1 class="page-header">bootstrap</h1>
    <!-- 路径导航 -->
    <ol class="breadcrumb">
        <li><a href="">bootstrap</a></li>
        <li><a href="">bootstrap</a></li>
        <li><a href="">bootstrap</a></li>
        <li class="active">bootstrap</li>
    </ol>
    <!-- 分页 -->
    <ul class="pagination">
        <li class="disabled"><a href="">&laquo;</a></li>
        <li class="active"><a href="">1</a></li>
        <li><a href="">2</a></li>
        <li><a href="">3</a></li>
        <li><a href="">4</a></li>
        <li class="pagination-lg"><a href="">&raquo;</a></li>
    </ul>
    <!-- 上下页 -->
    <ul class="pager">
        <li class="previous disabled"><a href=""><span>&larr;</span>上一页</a></li>
        <li class="next"><a href="">下一页<span>&rarr;</span></a></li>
    </ul>
    <!-- 标签 -->
    <span class="label label-primary">primary</span>
    <span class="label label-info">info </span>

    <!-- 徽章 -->
    <p></p>
    <a href="#">Inbox <span class="badge">42</span></a>
    <button class="btn btn-primary" type="button">
      Messages <span class="badge">4</span>
    </button>
    <p></p>
    <!-- 巨幕 -->
    <div class="jumbotron">
        <h1>bootstrap</h1>
        <p>bootstrap is vary goodbootstrap is vary goodbootstrap is vary goodbootstrap is vary goodbootstrap is vary goodbootstrap is vary goodbootstrap is vary goodbootstrap is vary goodbootstrap is vary goodbootstrap is vary goodbootstrap is vary good</p>
    </div>
    <!-- 自定义内容 -->
    <div class="row">
        <div class="col-sm-3">
            <div class="thumbnail">
            <img src="holder.js/100%x180">
                <div class="caption">
                <h2>Thumbnail label</h2>
                <p>bootstrap is very goodbootstrap is very goodbootstrap is very goodbootstrap is very goodbootstrap is very good</p>
                <p><a href="#" class="btn btn-primary" role="button">Button</a> <a href="#" class="btn btn-default" role="button">Button</a></p>
                </div>
            </div>
        </div>
        <div class="col-sm-3">
            <div class="thumbnail">
            <img src="holder.js/100%x180">
                <div class="caption">
                <h2>Thumbnail label</h2>
                <p>bootstrap is very goodbootstrap is very goodbootstrap is very goodbootstrap is very goodbootstrap is very good</p>
                <p><a href="#" class="btn btn-primary" role="button">Button</a> <a href="#" class="btn btn-default" role="button">Button</a></p>
                </div>
                </div>
        </div>
        <div class="col-sm-3">
            <div class="thumbnail">
            <img src="holder.js/100%x180">
                <div class="caption">
                <h2>Thumbnail label</h2>
                <p>bootstrap is very goodbootstrap is very goodbootstrap is very goodbootstrap is very goodbootstrap is very good</p>
                <p><a href="#" class="btn btn-primary" role="button">Button</a> <a href="#" class="btn btn-default" role="button">Button</a></p>
                </div>
                </div>
        </div>
        <div class="col-sm-3">
            <div class="thumbnail">
            <img src="holder.js/100%x180">
                <div class="caption">
                <h2>Thumbnail label</h2>
                <p>bootstrap is very goodbootstrap is very goodbootstrap is very goodbootstrap is very goodbootstrap is very good</p>
                <p><a href="#" class="btn btn-primary" role="button">Button</a> <a href="#" class="btn btn-default" role="button">Button</a></p>
                </div>
                </div>
        </div>
    </div>
    <!-- 警告框 -->
    <div class="alert alert-success">
    <!-- 关闭按钮 -->
    <span class="close" data-dismiss='alert'>&times;</span>
    <a href="#" class="alert-link">bootstrap</a> bootstrapbootstrapbootstrapbootstrapbootstrapbootstrapbootstrapbootstrapbootstrapbootstrapbootstrapbootstrapbootstrapbootstrapbootstrap</div>
    <div class="alert alert-info">
    <span class="close" data-dismiss='alert'>&times;</span>
    .bootstrapbootstrapbootstrapbootstrapbootstrapbootstrapbootstrapbootstrapbootstrapbootstrapbootstrapbootstrapbootstra</div>
    <div class="alert alert-warning">
    <span class="close" data-dismiss='alert'>&times;</span>
    bootstrapbootstrapbootstrapbootstrapbootstrapbootstrapbootstrapbootstrapbootstrapbootstrapbootstrapbootstrap</div>
    <div class="alert alert-danger">
    <span class="close" data-dismiss='alert'>&times;</span>
    bootstrapbootstrapbootstrapbootstrapbootstrapbootstrapbootstrapbootstrapbootstrapbootstrapbootstrapbootstrapb</div>
    <!-- 进度条 -->
    <div class="progress">
        <div class="progress-bar progress-start progress-bar-striped active" style="width: 0%"></div>
    </div>
    <div class="progress">
        <div class="progress-bar ogress-bar-striped" style="width: 90%">90%</div>
    </div>
    <div class="progress">
        <div class="progress-bar progress-bar-success progress-bar-striped " style="width: 40%">40%</div>
    </div>
    <div class="progress">
        <div class="progress-bar progress-bar-info progress-bar-striped"  style="width: 20%">20%</div>
    </div>
    <div class="progress">
        <div class="progress-bar progress-bar-warning progress-bar-striped active" style="width: 60%">60%</div>
    </div>
    <div class="progress">
        <div class="progress-bar progress-bar-danger progress-bar-striped active" style="width: 80%">80%</div>
    </div>
</div>
</body>
<script>
    s=0;v=1;
    sobj=setInterval(function(){
        s+=v;
        if(s>=100){
            clearInterval(sobj);
            $('.progress-start').removeClass('active');
        }
        $('.progress-start').html(s+'%').css({'width':s+'%'});
    },100);
</script>
</html>

```
## [演示地址](http://www.guliansheng.club/bootstrap3/10.网页元素.html)
