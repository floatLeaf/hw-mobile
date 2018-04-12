## picker<hr>
picker是一个JS实现的类似select的组件，他可以代替原生的select组件，并且功能更加强大、样式更加统一。

picker 需要初始化才能使用，你可以在一个 `input` 元素上初始化picker，当用户点击input的时候会弹出picker的弹层

picker 会自动读取 input 的value作为初始值。对于有多个cols的情况，可能初始值无法正确解析，因为picker并不知道该如何进行分割。默认的规则是：多列模式下，会把input中的值以空格分隔作为每一列的值。如果你有多列并且不是以空格分隔的，那么你需要自己通过参数传入这个初始值，而不能通过 input 元素的 value属性设置。
```
<input type="text" id='picker'/>
<script>
$("#picker").picker({
  title: "请选择您的手机",
  cols: [
    {
      textAlign: 'center',
      values: ['iPhone 4', 'iPhone 4S', 'iPhone 5', 'iPhone 5S', 'iPhone 6', 'iPhone 6 Plus', 'iPad 2', 'iPad Retina', 'iPad Air', 'iPad mini', 'iPad mini 2', 'iPad mini 3']
    }
  ]
});
</script>
```
####关闭picker
在任何元素上加上一个 `.close-picker` 类，点击它就会关闭 Picker。

你也可以通过调用 `$.closePicker()` 或者 `$("#input").picker("close")`来关闭当前弹出的 Picker。

####picker参数
你可以通过设置 `toolbarTemplate` 参数来自定义工具栏模板。在 cols 参数中可以传入多列值。
```
$("#picker-name").picker({
  title: "请选择您的称呼",
  cols: [
    {
      textAlign: 'center',
      values: ['赵', '钱', '孙', '李', '周', '吴', '郑', '王']
      //如果你希望显示文案和实际值不同，可以在这里加一个displayValues: [.....]
    },
    {
      textAlign: 'center',
      values: ['杰伦', '磊', '明', '小鹏', '燕姿', '菲菲', 'Baby']
    },
    {
      textAlign: 'center',
      values: ['先生', '小姐']
    }
  ]
});
```
所有可用参数如下：

|参数名	         | 默认值	|说明|
|title	         | "请选择"	|Picker 的标题|
|toolbarCloseText | 完成	| 关闭按钮的文案|
|toolbarTemplate  |请参见源码	|工具栏的模板，可以自己定义。|
|value		   |           |  Array with initial values. Each array item represents value of related column. Picker will auto read value from input if not set.|
|rotateEffect	  |false	        |是否启用3D效果，启用3D可能会影响性能|
|toolbar	  |true	        |是否显示工具栏|
|inputReadOnly	  |true	        |是否会在input上添加一个 readonly 属性|
|cssClass	  |undefined	|为 picker 容器增加额外的类，可以用来自定义样式|
|onChange	  |undefined	|当选择值改变的时候触发|
|onClose	  |undefined	|当picker被关闭时触发|

picker方法
你可以通过 `$("#input").picker("method", args1, args2...) `的方式来调用相关的方法。
```
$("#picker-name").picker("open");
$("#picker-name").picker("close");
$("#picker-name").picker("setValue", ["2012", "12", "12"]);
```
所有可用方法如下：

|方法名	      |参数说明	                                      |方法说明|
|------------ | -------------------------------------------- |------|
|open	      |无	                                     | 打开picker|
|close	      |无	                                      |关闭picker|
|setValue     |一个字符串数组，其中每个字符串对应每一列	      |设置值，请注意，只能设置在 config 中配置的那些值，无法设置一个不存在的新值。|

####内联模式
从 V0.8.0 版本开始，可以使用内联模式，只需要在初始化的时候指定一个 container 参数即可，picker会自动在这个容器中初始化。时间日期选择器以及地址选择器等因为继承自 picker，因此也都支持完全相同的内联模式。
```
$.picker({
  input: '#input',
  container: '#container'
})
```
注意，内联模式只是指定了容器，因此 input 参数还是必须的，而且强烈建议通过 input 来获取用户输入的值。如果你不希望显示一个输入框，可以把它设置成 `type="hidden"`。



