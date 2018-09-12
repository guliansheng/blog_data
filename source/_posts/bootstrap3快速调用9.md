---
title: bootstrap3快速调用9
date: 2018-09-11 19:14:34
tags:
    - 模态框
    - 弹出框
    - 标签页导航
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
    <h1>模态框</h1>
    <hr>
    <!-- Button trigger modal -->
    <button type="button" class="btn btn-primary btn-lg smodal" data-target="#myModal">
      Launch demo modal
    </button>
    <!-- Modal模态框内容 -->
    <div class="modal fade" id="myModal"><!-- fade类是模态框淡入淡出动画类 -->
    <!-- 模态框的尺寸:在.modal-dialog后面添加modal-lg或者modal-sm分别表示大和小，不添加则是默认中等大小 -->
      <div class="modal-dialog modal-sm">
        <div class="modal-content">
          <div class="modal-header"><!-- 头部 -->
            <button type="button" class="close hmodal"><span>&times;</span></button><!-- 关闭符号 -->
            <h4 class="modal-title" id="myModalLabel">Modal title</h4>
          </div>
          <div class="modal-body"><!-- 体部 -->
            Linux is very good !Linux is very good !Linux is very good !Linux is very good !Linux is very good !Linux is very good !Linux is very good !Linux is very good !Linux is very good !Linux is very good !Linux is very good !Linux is very good !Linux is very good !Linux is very good !Linux is very good !Linux is very good !Linux is very good !Linux is very good !Linux is very good !Linux is very good !Linux is very good !Linux is very good !Linux is very good !Linux is very good !Linux is very good !Linux is very good !Linux is very good !Linux is very good !Linux is very good !Linux is very good !Linux is very good !Linux is very good !Linux is very good !Linux is very good !Linux is very good !Linux is very good !Linux is very good !Linux is very good !Linux is very good !Linux is very good !Linux is very good !Linux is very good !Linux is very good !
          </div>
          <div class="modal-footer"><!-- 底部 -->
            <button type="button" class="btn btn-default hmodal">Close</button><!-- 关闭按钮 -->
            <button type="button" class="btn btn-primary savemodal">Save changes</button>
          </div>
        </div>
      </div>
    </div>
    <p></p>
    <!-- 标签页导航 -->
    <ul class="nav nav-tabs">
        <li class="active"><a href="#php" data-toggle='tab'>php</a></li>
        <li><a href="#js" data-toggle='tab'>js</a></li>
        <li><a href="#java" data-toggle='tab'>java</a></li>
    </ul>
    <div class="tab-content">
        <div id='php' class="tab-pane active fade in"><!-- fade in 淡入效果 -->
            Raw denim you probably haven't heard of them jean shorts Austin. Nesciunt tofu stumptown aliqua, retro synth master cleanse. Mustache cliche tempor, williamsburg carles vegan helvetica. Reprehenderit butcher retro keffiyeh dreamcatcher synth. Cosby sweater eu banh mi, qui irure terry richardson ex squid. Aliquip placeat salvia cillum iphone. Seitan aliquip quis cardigan american apparel, butcher voluptate nisi qui.
        </div>
        <div id='js' class="tab-pane fade">
            Food truck fixie locavore, accusamus mcsweeney's marfa nulla single-origin coffee squid. Exercitation +1 labore velit, blog sartorial PBR leggings next level wes anderson artisan four loko farm-to-table craft beer twee. Qui photo booth letterpress, commodo enim craft beer mlkshk aliquip jean shorts ullamco ad vinyl cillum PBR. Homo nostrud organic, assumenda labore aesthetic magna delectus mollit. Keytar helvetica VHS salvia yr, vero magna velit sapiente labore stumptown. Vegan fanny pack odio cillum wes anderson 8-bit, sustainable jean shorts beard ut DIY ethical culpa terry richardson biodiesel. Art party scenester stumptown, tumblr butcher vero sint qui sapiente accusamus tattooed echo park.
        </div>
        <div id='java' class="tab-pane fade">
            Etsy mixtape wayfarers, ethical wes anderson tofu before they sold out mcsweeney's organic lomo retro fanny pack lo-fi farm-to-table readymade. Messenger bag gentrify pitchfork tattooed craft beer, iphone skateboard locavore carles etsy salvia banksy hoodie helvetica. DIY synth PBR banksy irony. Leggings gentrify squid 8-bit cred pitchfork. Williamsburg banh mi whatever gluten-free, carles pitchfork biodiesel fixie etsy retro mlkshk vice blog. Scenester cred you probably haven't heard of them, vinyl craft beer blog stumptown. Pitchfork sustainable tofu synth chambray yr.
        </div>
    </div>
</div>

</body>
<script type="text/javascript">
//关闭和打开模态框方法：.modal('show')和modal('hide'),modal('toggle')打开或关闭;
$('.smodal').click(function () {
    $('#myModal').modal('show');
})
$('.hmodal').click(function(){
    $('#myModal').modal('hide');
})
//事件：show.bs.modal:show方法调用之前;shown.bs.modal:模态框显示出来之后;hide.bs.modal:hide方法调用之前;hiden.bs.modal:模态框隐藏之后;
$('#myModal').on('hidden.bs.modal', function () {
    $('body').css({'background':'#ccc'});
})

</script>
</html>


```

## [演示地址](http://www.guliansheng.club/bootstrap3/12.模态框弹出框.html)

