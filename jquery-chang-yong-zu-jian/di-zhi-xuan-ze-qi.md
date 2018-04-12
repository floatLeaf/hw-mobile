##地址选择器
v0.8.1 的用户请尽快升级到 v0.8.2，修复了地址选择器 onChange 函数参数的bug。

地址选择器需要引入额外的JS文件：
```
<script type="text/javascript" src="js/city-picker.js" charset="utf-8"></script>
```
地址选择器是一个定制的 picker，所以其用法和 Picker 是一样的。

从 v0.8.1+ 版本开始，可以设置除了 cols 和 cssClass 之外的全部picker中的参数。
```
<input type="text" id='city-picker'/>
<script>
  $("#city-picker").cityPicker({
    title: "请选择收货地址"
  });
</script>
```
input 的 value 属性可以设置默认值，以空格分割。
```
<input type="text" id='city-picker' value="浙江 杭州 拱墅区" />
```
####参数
除了 `Picker` 的全部参数可用之外，`city-picker` 还有如下参数可以配置:

|参数名	       | 默认值	|说明|
|--------------|-------|---|
|showDistrict	|true	|是否显示地区|

比如如下设置可以不显示地区（只选择省市):
```
//禁用地区选择
$("#city-picker").cityPicker({
  showDistrict: false
});
```
你可以通过 `$.fn.cityPicker.prototype.defaults` 来改变默认值。

地区编码
从 v0.8.1 版本开始支持地区编码，编码来自 国家统计局发布的数据。

版本升级!重要！
特别注意， v0.8.1+ 版本除了增加了地区编码之外，省市的名字也发生了变化，主要变化是加上了 '省' 和 '市' 的后缀，所以以前的数据如果用在 v0.8.1+ 版本会导致无法匹配。