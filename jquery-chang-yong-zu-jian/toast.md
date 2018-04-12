##Toast
Toast 用于临时显示某些信息，并且会在数秒后自动消失。这些信息通常是轻量级操作的成功、失败或等待状态信息。

Toast 只能通过 JavaScript 进行调用:
```
$.toast();
$.toast("操作成功");
```
Toast 有三种模式可以选择，默认是 成功 模式，还有 取消 和 禁止 两种模式:

从 V0.7.1 版本开始，新增了一个纯文本模式。
```
$.toast("取消操作", "cancel");
$.toast("禁止操作", "forbidden");
$.toast("纯文本", "text");
// 第二个参数可以是时间，单位毫秒
$.toast("消息", 20000);
```
####参数
Toast 默认时间是 2000 毫秒，可以通过 $.toast.prototype.defaults.duration 来设置这个值。

回调函数
toast可以指定一个回调函数，当toast关闭的时候会调用此函数。
```
$.toast("取消操作", function() {
  console.log("cancel");
});
$.toast("禁止操作", "forbidden", function() {
  //do something
});
```