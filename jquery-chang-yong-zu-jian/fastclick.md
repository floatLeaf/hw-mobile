##fastclick <hr>
iOS 系统下默认的 click 事件会有300毫秒的延迟，这个延迟是iOS系统的特性而不是jQuery WeUI设定的，可以使用 fastclick 来消除这个延迟。

jQuery WeUI 是不包含 fastclick 的，你只需要按照标准的用法引用并初始化即可，可以参考以下代码：
```
<script src="../lib/fastclick.js"></script>
<script>
  $(function() {
    FastClick.attach(document.body);
  });
</script>
···
在官方 demos 中是引入了 fastclick ，可以参考其中的代码。

关于更多 fastclick 相关的文档，请移步其官网 [https://github.com/ftlabs/fastclick](https://github.com/ftlabs/fastclick)

注意，从 V0.8.1 开始支持 fastclick，在以前版本引入会导致个别组件出现无法点击的情况。