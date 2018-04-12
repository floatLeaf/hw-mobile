### 滚动加载<hr>
当用户滚动到页面底部的时候加载更多内容。

首先你需要把一段显示加载状态的代码放入需要滚动加载的容器中，这里我们默认是 document.body，加载指示器的代码如下：
```
<div class="weui-loadmore">
  <i class="weui-loading"></i>
  <span class="weui-loadmore__tips">正在加载</span>
</div>

```

然后调用JS初始化滚动加载插件：
```
$(document.body).infinite();
```
从 v0.4.0 版本开始，可以在任何div内初始化滚动加载组件，并且一个页面内可以初始化多个。

####参数
infinite 方法接收一个 distance 参数：
```
$(document.body).infinite(100);
```
默认的 distance 值是 50，表示滚动到距离底部 50 px 的时候会触发加载.

####事件
当用户滚动到页面底部的时候，会在 body 上触发 infinite 事件。监听此事件即可:
```
var loading = false;  //状态标记
$(document.body).infinite().on("infinite", function() {
  if(loading) return;
  loading = true;
  setTimeout(function() {
    $("#list").append("<p> 我是新加载的内容 </p>");
    loading = false;
  }, 1500);   //模拟延迟
});
```

**注意一点，因为插件并不知道你是否正在加载，所以只要滚动到距离底部 50px 以内都会触发事件。因此 infinite 事件可能会触发多次。需要自己来控制不要同时进行多个加载。可以参考上面的代码通过一个 loading 标记位来控制。**

####销毁
如果你不需要滚动加载了，比如已经加载完了所有内容，调用 $(document.body).destroyInfinite() 可以销毁插件。之后你可以再次调用 $(document.body).infinite() 来重新初始化.

不过即使销毁插件，也不会把加载指示器的HTML代码删除，所以你需要自己来隐藏或者删除它。

####滚动加载结合TAB
同样可以在每一个 .weui-tab__bd-item 都初始化一个独立的滚动加载：
```
<div class="weui-tab" id='page-infinite-navbar'>
  <div class="weui-navbar">
    <a href='#tab1' class="weui-navbar__item weui-bar__item--on">
      选项一
    </a>
    <a href='#tab2' class="weui-navbar__item">
      选项二
    </a>
  </div>
  <div class="weui-tab__bd">
    <div id="tab1" class="weui-tab__bd-item weui-tab__bd-item--active">
      <h1 class="doc-head">页面一</h1>
      <div class="content-padded">
        ...
      </div>
      <div class="weui-infinite-scroll">
        <div class="infinite-preloader"></div>
        正在加载...
      </div>
    </div>
    <div id="tab2" class="weui-tab__bd-item">
      <h1 class="doc-head">页面二</h1>
      <div class="content-padded">
        ...
      </div>
      <div class="weui-infinite-scroll">
        <div class="infinite-preloader"></div>
        正在加载...
      </div>
    </div>
  </div>
</div>
```