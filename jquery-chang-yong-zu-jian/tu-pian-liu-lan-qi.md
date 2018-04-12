##Photo Browser<hr>
为了使用图片浏览器，你必须引用如下的JS文件：
```
<script type='text/javascript' src='/js/swiper.js' charset='utf-8'></script>
Photo Browser 是一个可以全屏浏览多张图片的插件，类似朋友圈中查看图片的功能。
```
Photo Browser 只能通过 JavaScript 进行调用:
```
var pb1 = $.photoBrowser({
  items: [
    "./images/swiper-1.jpg",
    "./images/swiper-2.jpg",
    "./images/swiper-3.jpg"
  ]
});
```
如果图片带有文案，可以这样调用：
```
var pb2 = $.photoBrowser({
  items: [
    {
      image: "./images/swiper-1.jpg",
      caption: "描述文案"
    },
    {
      image: "./images/swiper-2.jpg",
      caption: "描述文案"
    },
    {
      image: "./images/swiper-3.jpg",
      caption: "描述文案"
    }
  ]
});
```
`$.photoBrowser` 方法会返回一个实例，这个实例可以调用方法打开和关闭弹层：
```
pb.open();  //打开
pb.close(); //关闭
```
####参数配置
`$.photoBrowser(config)` 有如下配置可用：

|参数名	        |说明	                                              |示例|
| ------------- | -------------------------------------------------- |---|
|items	        |需要展示的图片	                                      |items: ["./images/swiper-1.jpg", "./images/swiper-2.jpg", ...]|
|onSlideChange	|左右翻页的回调函数	                               |onSlideChange: function(index) { console.log(index); }|
|onOpen	        |每次打开之后执行回调	                               |onOpen: function() { console.log(this); }|
|onClose	|每次关闭之后执行回调	                               |onClose: function() { console.log(this); }|
|tpl	        |图片浏览器的HTML模板，除非非常熟悉，否则不建议直接修改模板	 |                                         |
|initIndex	|初始化显示第几张，从0开始。 V0.7.1版本开始才支持此参数。   |                                          |

**注意，请不要使用上述列表没有列出来的配置，因为这些没有列出来的是下一个版本很可能会改动的，包括 swiper 对象可能会被删除。**

####属性和方法
`$.photoBrowser`会返回一个 photos 实例，这个实例上有如下方法和属性可以使用：

|方法/属性	               |说明|
|---------------------------- |----|
|open(index)	               |打开图片浏览器，可以传入一个可选的 index 参数来指定打开后默认显示的图片(从0开始)|
|close()	               |关闭图片浏览器|
|slideTo(index, duration)	|滚动到指定图片|
|slidePrev()	               |滚动到上一张图片|
|slideNext()	               |滚动到下一张图片|
|activeIndex	               |当前显示的图片|
|currentScale	               |当前缩放比例|

为了调用以上方法，请确保您的版本为 V0.8.0 或者更新。其中所有属性都是只读的，请不要随意修改。请不要调用上述未列出的任何方法，因为这些方法都是内部使用的。

注意，从 V0.7.0 开始才支持 photos 组件。

