##Swiper<hr>

为了使用幻灯片，你必须引用如下的JS文件：
```
<script type='text/javascript' src='/js/swiper.js' charset='utf-8'></script>
```
在 Swiper 容器上调用 $(".swiper-container").swiper(config) 来初始化.
```
<div class="swiper-container" data-space-between='10' data-pagination='.swiper-pagination' data-autoplay="1000">
  <div class="swiper-wrapper">
    <div class="swiper-slide"><img src="//gqianniu.alicdn.com/bao/uploaded/i4//tfscom/i1/TB1n3rZHFXXXXX9XFXXXXXXXXXX_!!0-item_pic.jpg_320x320q60.jpg" alt=""></div>
    <div class="swiper-slide"><img src="//gqianniu.alicdn.com/bao/uploaded/i4//tfscom/i4/TB10rkPGVXXXXXGapXXXXXXXXXX_!!0-item_pic.jpg_320x320q60.jpg" alt=""></div>
    <div class="swiper-slide"><img src="//gqianniu.alicdn.com/bao/uploaded/i4//tfscom/i1/TB1kQI3HpXXXXbSXFXXXXXXXXXX_!!0-item_pic.jpg_320x320q60.jpg" alt=""></div>
  </div>
</div>
```
####配置
你可以通过 data-xxx 属性的方式在 .swiper-container 上写配置, 也可以通过 $().swiper(config) 的 config 参数来设置。Swiper 是对第三方插件的一个简单封装，更多文档请参阅 Swiper 官方文档