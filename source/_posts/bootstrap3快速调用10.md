---
title: bootstrap3快速调用10
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
    <link rel="stylesheet" type="text/css" href="./bs/css/bootstrap.css">
    <script type="text/javascript" src='./bs/js/jquery.js'></script>
    <script type="text/javascript" src='./bs/js/bootstrap.js'></script>
    <script type="text/javascript" src='./bs/js/docs.js'></script>
</head>
<body>
<div class="container">
<h1>工具提示<small>必须加入docs.js才能用</small></h1>
<img src="holder.js/100%x300" alt=""> <!-- docs.js同样可以使用holder.js的效果 -->
<div class="tooltip-demo"><!-- 必须放在这个div中才能使用工具提示 -->
      <button type="button" class="btn btn-default" data-toggle="tooltip" data-placement="left" title="Tooltip on left">Tooltip on left</button>
      <button type="button" class="btn btn-default" data-toggle="tooltip" data-placement="top" title="" data-original-title="Tooltip on top">Tooltip on top</button>
      <button type="button" class="btn btn-default" data-toggle="tooltip" data-placement="bottom" title="" data-original-title="Tooltip on bottom">Tooltip on bottom</button>
      <button type="button" class="btn btn-default" data-toggle="tooltip" data-placement="right" title="" data-original-title="Tooltip on right" aria-describedby="tooltip274325">Tooltip on right</button>
      <span data-toggle="tooltip" data-placement="left" title="弹出的内容放在title中">应用在其他标签</span>
</div>
<h1>弹框</h1>
<div class="popover-demo"><!-- 必须放在该div中,点击按钮可出现消失弹框 -->
    <button type="button" class="btn btn-default"  data-toggle="popover" data-placement="top" data-content="Vivamus sagittis lacus vel augue laoreet rutrum faucibus." title='顶部弹框'>
    Popover on 顶部
    </button>
    <button type="button" class="btn btn-default"  data-toggle="popover" data-placement="bottom"  data-content="Vivamus
    sagittis lacus vel augue laoreet rutrum faucibus.">
    Popover on 底部
    </button>
</div>
<h1>可消失弹框</h1>
<div class="bs-example-padded-bottom"><!-- 同样要放在这个div中 -->
    <a tabindex="0" class="btn btn-lg btn-danger bs-docs-popover"  data-toggle="popover" data-trigger="focus" title="Dismissible popover" data-content="And here's some amazing content. It's very engaging. Right?" >可消失的弹出框</a>
</div>
<p></p>
<p></p>
<p></p>
</div>
</body>
</html>

```
## [演示地址](http://www.guliansheng.club/bootstrap3/14.工具提示和弹框.html)
