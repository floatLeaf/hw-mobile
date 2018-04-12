##通知
模仿iOS风格的通知。你可以自定义标题，文案和图标。通过滑动手势可以关闭。

使用JS来打开和关闭通知:
````  
$.notification({
  title: "Baby",
  text: "I miss you",
  media: "<img src='...'>",
  data: "123",
  onClick: function(data) {
    $.alert("Click" + data);
  },
  onClose: function(data) {
    $.alert("Close "+data);
  }
});

//close notification

$.closeNotification();
```
一次只能显示一个通知，如果在前一个通知未消失的情况下显示下一个通知。则下一个通知会直接替换掉前一个通知

####Params
|Param	|Default	|Description|
|-------|--------------|-----------|
|title	|undefined	|通知的标题|
|text	|undefined	|通知的文案|
|media	|undefined	|图标|
|data	|undefined	|点击通知后，这个data参数会传给 onClick|
|onClick	|undefined	|点击回调|
|onClose	|undefined	|关闭通知的回调|
|time	|4000	|自动消失的时间|