---
title: bootstrap3快速调用2
date: 2018-09-11 17:18:28
tags: 
    - bootstrap
    - 表单
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
    </style>
</head>
<body>
<div class="container">
<h1 class="page-header">bootstrap</h1>
<form action="">
    <div class="form-group ">
        <label>用户名：</label>
        <input type="text" class="form-control" placeholder="username" maxlength="6">
    </div>
    <div class="form-group">
        <label>密码：</label>
        <input type="password" class="form-control"  placeholder="password" maxlength="8">
    </div>
    <div class="form-group">
        <!-- 文本域cols控制文本列数，rows控制文本行数，resize控制文本域是否可变大小 -->
        <textarea class="form-control" rows='10' style="resize: none;"></textarea>
    </div>
    <div class="form-group">
        <select class="form-control" size="2" multiple>
            <option value="城市">北京</option>
            <option value="城市">北京</option>
            <option value="城市">北京</option>
            <option value="城市">北京</option>
        </select>
    </div>
    <div class="form-group">
        <label class="checkbox-inline"><input type="checkbox" name="" disabled>篮球</label>
        <label class="checkbox-inline"><input type="checkbox" name="">篮球</label>
        <label class="checkbox-inline"><input type="checkbox" name="" checked>篮球</label>
        <label class="checkbox-inline"><input type="checkbox" name="">篮球</label>
    </div>
    <div class="form-group">
        <label class="radio-inline"><input name='zq' type="radio">足球</label>
    </div>
    <div class="form-group">
        <label class="radio-inline"><input name='zq' type="radio">足球</label>
    </div>
    <div class="form-group">
        <label class="radio-inline"><input name="zq" type="radio">足球</label>
    </div>
    <div class="form-group">
        <label class="radio-inline"><input name="zq" type="radio">足球</label>
    </div>
    <div class="form-group has-feedback">
        <!--input-group 输入框组 ，内部文字放在类input-group-addon div中,输入框不用添加类input-group-addon-->
        <div class="input-group ">
            <div class="input-group-addon">$</div>
            <input type="text" class="form-control">
        </div>
        <span class="form-control-feedback glyphicon glyphicon-tags"></span>
    </div>
    <div class="form-group">
        <input type="submit" value="Ok" class="btn btn-primary btn-sm">
        <input type="reset" value="Concel" class="btn btn-danger btn-sm">
    </div>
</form>
<!-- 列表横排 -->
<form class="form-inline">
    <div class="form-group">
        <input type="text" class="form-control">
    </div>
    <div class="form-group">
        <input type="text" class="form-control">
    </div>
</form>
<br>
<!-- 水平排列列表 -->
<form action="" class="form-horizontal">
<div class="form-group has-success has-feedback">
<!-- label内的文字会加粗 -->
    <label class="col-sm-2 control-label">用户名</label>
    <div class="col-sm-6">
        <input type="text" class="form-control">
        <span class="glyphicon glyphicon-user form-control-feedback" aria-hidden='true'></span>
    </div>
</div>
<div class="form-group has-error has-feedback">
    <label class="col-sm-2 control-label">密码</label>
    <div class="col-sm-6">
        <input type="text" class="form-control">
        <span class=" glyphicon glyphicon-remove form-control-feedback"></span>
    </div>
</div>
<!-- form-control-static可以将表单中的p标签中的文字对其排列 -->
<div class="form-group has-warning">
    <label class="col-sm-2 control-label">邮箱</label>
    <div class="col-sm-10 ">
        <p class=" form-control-static">272889889@qq.com</p>
    </div>
</div>
<div class="col-sm-8 col-sm-offset-2">
    <div class="form-group has-success has-feedback">
      <label class="control-label">Input group with success</label>
      <div class="input-group">
        <span class="input-group-addon">@</span>
        <input type="text" class="form-control">
      </div>
      <span class="glyphicon glyphicon-ok form-control-feedback"></span><p class="help-block">表单框帮助提示</p>
    </div>
</div>
<div class="form-group">
    <div class="col-sm-10 col-sm-offset-2">
        <input type="submit" value="Ok" class='btn btn-primary btn-sm'>
        <input type="reset" value="Concel" class="btn btn-danger btn-sm">

    </div>

</div>
</form>
</div>
</body>
```
## [演示地址](http://www.guliansheng.club/bootstrap3/4.表单.html)
