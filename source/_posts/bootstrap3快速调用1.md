---
title: bootstrap3快速调用1
date: 2018-09-11 15:47:51
tags: 
    - bootstrap
    - 表格
    - 按钮
    - 排版
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
    <link rel="stylesheet" href="./bs/js/jquery.js">
    <link rel="stylesheet" href="./bs/js/bootstrap.js">
    <style type="text/css">
    .ul2{
        height: 40px;
    }
    .ul2 li{
        width: 100px;
        height: 40px;
        float: left;
    }
    mark{
        background: #a2f0f0;
    }
    </style>
</head>
<body>
<div class="container">
    <h1 class="page-header">bootstrap <small>作者：gu</small></h1>
    <p class="lead text-justify">bootstrap is very good!bootstrap is very good!<del>bootstrap is very good!</del><mark>bootstrap is very good!</mark>bootstrap is very good!<small>bootstrap is very good!</small>bootstrap is very good!bootstrap is very good!bootstrap is very good!bootstrap is very good!bootstrap is very good!bootstrap is very good!bootstrap is very good!bootstrap is very good!bootstrap is very good!bootstrap is very good!bootstrap is very good!</p>
    <p class="page-header text-center">bootstrap</p>
    <dl>
        <dt>选择题：</dt>
        <dd>a.bootstrap</dd>
        <dd>a.bootstrap</dd>
        <dd>a.bootstrap</dd>
        <dd>a.bootstrap</dd>
        <dt>选择题：</dt>
        <dd>a.bootstrap</dd>
        <dd>a.bootstrap</dd>
        <dd>a.bootstrap</dd>
        <dd>a.bootstrap</dd>
    </dl>
    <dl class="dl-horizontal">
        <dt>选择题：</dt>
        <dd>a.bootstrap</dd>
        <dd>a.bootstrap</dd>
        <dd>a.bootstrap</dd>
        <dd>a.bootstrap</dd>
        <dt>选择题：</dt>
        <dd>a.bootstrap</dd>
        <dd>a.bootstrap</dd>
        <dd>a.bootstrap</dd>
        <dd>a.bootstrap</dd>
    </dl>
    <!-- 无样式列表，同时去除ul内部padding -->
    <ul class="list-unstyled">
        <li>list</li>
        <li>list</li>
        <li>list</li>
        <li>list</li>
        <li>list</li>
    </ul>
    <ul class="list-inline ul2">
        <li>first</li>
        <li>last</li>
        <li>last</li>
        <li>last</li>
    </ul>
    <p>is very<code>section</code> good</p>
    <p>按下<kbd>ctrl+shift</kbd></p>
    <samp>This text is meant to be treated as sample output from a computer program.</samp>
    <p><pre>
        如果要原样输出html代码，则<,>要用编码形式;
        if(i<0){
        return false;
        }
    </pre></p>
    <p>未用pre标签：if(i<0){
        return false;
        }
    </p>

    <div class="table-responsive"><!-- 响应式表格，当列数少时不会出现横向滚动条 -->
          <table class="table table-striped table-hover table-bordered ">
            <tr>
                <th>ID</th>
                <th>用户名</th>
                <th>密码</th>
                <th>ID</th>
                <th>用户名</th>
                <th>密码</th>
            </tr>
            <tr>
                <td>1</td>
                <td>2</td>
                <td>3</td>
                <td>1</td>
                <td>2</td>
                <td>3</td>
            </tr>
            <tr >
                <td>1</td>
                <td>2</td>
                <td>3</td>
                <td>1</td>
                <td>2</td>
                <td>3</td>
            </tr>
            <tr class="success">
                <td>1</td>
                <td>2</td>
                <td>3</td>
                <td>1</td>
                <td>2</td>
                <td>3</td>
            </tr>
            <tr class="info">
                <td>1</td>
                <td>2</td>
                <td>3</td>
                <td>1</td>
                <td>2</td>
                <td>3</td>
            </tr>
            <tr class="warning">
                <td>1</td>
                <td>2</td>
                <td>3</td>
                <td>1</td>
                <td>2</td>
                <td>3</td>
            </tr>
            <tr class="danger">
                <td>1</td>
                <td>2</td>
                <td>3</td>
                <td>1</td>
                <td>2</td>
                <td>3</td>
            </tr>
            <tr class="active">
                <td  class="warning">1</td>
                <td>2</td>
                <td>3</td>
                <td  class="warning">1</td>
                <td>2</td>
                <td>3</td>
            </tr>
          </table>
    </div>
    <p>
        <button class="btn btn-default btn-lg">default按钮</button>
        <button class="btn btn-primary">primary按钮</button>
        <button class="btn btn-success btn-sm">success按钮</button>
        <button class="btn btn-info btn-xs">info按钮</button>
        <button class="btn btn-warning ">warning按钮</button>
        <button class="btn btn-danger ">danger按钮</button>
        <button class="btn btn-link ">link按钮</button>
        <button class="btn btn-block btn-info">块级标签按钮</button>
        <button class="btn btn-danger active">激活状态</button>
        <button type="button" class="btn btn-primary" disabled>禁用状态</button>
    </p>
</div>

</body>
</html>
```

## [演示地址](http://www.guliansheng.club/bootstrap3/2.排版-表格-按钮-代码.html)
