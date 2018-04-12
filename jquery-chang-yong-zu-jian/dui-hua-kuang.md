##对话框<hr>
若系统的alert窗体无法满足网页的临时视图内容需求，则可以自定义实现与alert形式相似的dialog，并且在dialog中可以自定义地使用各种控件，来满足需求。

对话框只能通过 JavaScript 进行调用，我们提供了三种常用的对话框 Alert, Confirm, Prompt 和 Login. 你也可以通过 $.modal 来自定义对话框

实际上， Alert, Confirm, Prompt 和 Login 都是 Modal 的一种定制而已。

####Alert
显示一段警告消息，有一个确认按钮。
```
$.alert("自定义的消息内容");
$.alert("自定义的消息内容", "自定义的标题");
$.alert("自定义的消息内容", function() {
  //点击确认后的回调函数
});
$.alert("自定义的消息内容", "标题", function() {
  //点击确认后的回调函数
});

//如果参数过多，通过 object 方式传入
$.alert({
  title: '标题',
  text: '内容文案',
  onOK: function () {
    //点击确认
  }
});
```
####Confirm
显示一段确认消息，有一个确认按钮和一个取消按钮
```
$.confirm("自定义的消息内容");
$.confirm("自定义的消息内容", "自定义的标题");
$.confirm("自定义的消息内容", function() {
  //点击确认后的回调函数
  }, function() {
  //点击取消后的回调函数
  });


//如果参数过多，建议通过 object 方式传入
$.confirm({
  title: '标题',
  text: '内容文案',
  onOK: function () {
    //点击确认
  },
  onCancel: function () {
  }
});
```
####Prompt
显示一个带有输入框的对话框,可以让用户输入信息
```
$.prompt("自定义的消息内容", function(text) {
  //点击确认后的回调函数
  //text 是用户输入的内容
}, function() {
  //点击取消后的回调函数
});

//如果参数过多，建议通过 object 方式传入
$.prompt({
  title: '标题',
  text: '内容文案',
  input: '输入框默认值',
  empty: false, // 是否允许为空
  onOK: function (input) {
    //点击确认
  },
  onCancel: function () {
    //点击取消
  }
});
```

####Login
显示一个登录框：
```
$.login("自定义的消息内容", function(username, password) {
  // 这里进行登录操作
}, function() {
});

//如果参数过多，建议通过 object 方式传入
$.login({
  title: '标题',
  text: '内容文案',
  username: 'tom',  // 默认用户名
  password: 'tom',  // 默认密码
  onOK: function (username, password) {
    //点击确认
  },
  onCancel: function () {
    //点击取消
  }
});
```
登录框从 V0.8.0 版本可用。

####自定义对话框
上述的三种对话框都是 $.modal 的一种特殊形式。你可以通过 $.modal 来定制对话框:
```
$.modal({
  title: "Hello",
  text: "我是自定义的modal",
  buttons: [
    { text: "支付宝", onClick: function(){ console.log(1)} },
    { text: "微信支付", onClick: function(){ console.log(2)} },
    { text: "取消", className: "default", onClick: function(){ console.log(3)} },
  ]
});
```
####关闭对话框
默认情况下，点击对话框的按钮都会先关闭对话框再触发回调函数。

你可以通过JS来关闭任何正在显示的对话框:
```
$.closeModal();
```
####默认配置
对话框的默认是 $.modal.prototype.defaults，默认配置如下：
```
defaults = $.modal.prototype.defaults = {
  title: "提示",
  text: undefined,
  buttonOK: "确定",
  buttonCancel: "取消",
  buttons: [{
    text: "确定",
    className: "primary"
  }],
  autoClose: true //点击按钮自动关闭对话框，如果你不希望点击按钮就关闭对话框，可以把这个设置为false
};
```