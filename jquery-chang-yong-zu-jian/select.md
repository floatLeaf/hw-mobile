##Select<hr>
Select 是一种支持单选或者多选的弹出层，它可以用来代替原生的 select 元素提供更好更一致的用户体验。Select 是一个JS组件，只能通过JS方法来调用.

####简单用法
基本用法如下：
```
$("#job").select({
  title: "选择职业",
  items: ["法官", "医生", "猎人", "学生", "记者", "其他"]
});
```

####设置不同的显示值和实际值
Select 可以设置不用的显示值和实际值，很多时候显示给用户看的字符串和实际提交值是不同的，比如：
```
$("#mobile").select({
  title: "选择手机",
  items: [
    {
      title: "iPhone 3GS",
      value: "001",
    },
    {
      title: "iPhone 5",
      value: "002",
    },
    {
      title: "iPhone 5S",
      value: "003",
    },
    {
      title: "iPhone 6",
      value: "004",
    },
    {
      title: "iPhone 6S",
      value: "005",
    },
    {
      title: "iPhone 6P",
      value: "006",
    },
    {
      title: "iPhone 6SP",
      value: "007",
    },
    {
      title: "iPhone SE",
      value: "008",
    },
    {
      title: "iPhone 7",
      value: "009"
    }
  ]
});
```
当设置了不同的显示值和实际值时请注意，这个时候 input 的 value 依然是显示值，而实际值存储在 data-values 属性中。如果你设置了初始值，请保证同时设置了 value 和 data-values 两个值。

####多选
增加一个 multi: true 参数，就可以设置为多选:
```
$("#in").select({
  title: "您的爱好",
  multi: true,
  items: [
    {
      title: "画画",
      value: 1
    },
    {
      title: "打球",
      value: 2
    },
    {
      title: "唱歌",
      value: 3
    },
    {
      title: "游泳",
      value: 4
    },
  ]
});
```

####默认配置
Select 的默认配置是 $.fn.select.prototype.defaults:

|参数名	    |默认值	|说明|
|-----------|----------|----|
|input	    |undefined	|输入框的初始值，如果设置了这个值，那么他会覆盖 input 本身的 value 值。 从 V0.7.0 开始支持此配置。|
|autoClose	|true	|自动关闭，只有在单选模式下才可用，选择完成之后自动关闭弹窗|
|closeText	|"关闭"	|关闭按钮的文案|
|multi	    |false	|是否多选|
|max	    |undefined	|多选模式下，最多可选个数, V0.7.2|
|min	    |undefined	|多选模式下，最少可选个数, V0.7.2|
|split	      |","	|分隔符|
|title	    |"请选择"	|弹窗的标题|
|onChange	|undefined	|用户选择之后的回调，注意从 V0.6.1 版本之后才支持。你也可以在 input 上监听 `change` 事件。|
|onOpen	    |undefined	|弹层打开之后执行此回调函数。 V0.7.0 开始支持此配置|
|onClose	   | undefined	|弹层关闭之后执行此回调函数。 V0.7.0 开始支持此配置|
|beforeClose  |undefined	|弹层关闭之前执行此回调函数，如果返回 false 则可以阻止关闭。 V0.7.2|

你可以直接修改默认配置，但是建议通过 `$().select(config)` 的方式来配置。

####方法
通过 `$(xxx).select("method", args)` 方式可以调用 已经初始化完成 的select组件的方法。

全部可用方法如下:

|方法名	|示例	|说明|
|-------|------|-----|
|update	|$("input").select("update", { items: ["法官", "猎人", ...] })|	动态更新配置，传入的参数是一个 config 对象，初始化时候设定的任何参数都可以通过这种方式进行修改。|
|open	|$("input").select("open")	|打开弹层|
|close	|$("input").select("close")	|关闭弹层| 

**再次强调一点，必须是通过 $(input).select(config) 初始化之后才能调用对应的方法，否则请先初始化。**