##Popup
Popup 是一个覆盖式的弹出层，可以完全盖住当前页面。

Popup 需要一个模板，简单的模板如下:
```
<div id="" class="weui-popup__container">
  <div class="weui-popup__overlay"></div>
  <div class="weui-popup__modal">
    你的内容放在这里...
  </div>
</div>
```
然后可以通过设置一个链接，当点击的时候就会打开这个模板:
```
<a href="javascript:;" class="open-popup" data-target="">About</a>
```
其中 `class='open-popup'` 和 `data-target=""`两个属性不可缺少，前者表示点击链接需要打开一个 popup，后者是这个popup的选择器

当然，你也可以通过调用 JS 方法来打开一个 popup：
```
$("#about").popup();
```
####非全屏模式

在容器上增加一个类 `popup-bottom `即可：
```
<div id="" class="weui-popup__container popup-bottom">
  <div class="weui-popup__overlay"></div>
  <div class="weui-popup__modal">
    你的内容放在这里...
  </div>
</div>
```
####关闭 Popup
给任何链接加上 `class='close-popup'` 则点击之后可以关闭当前打开的 popup. 你也可以通过 $.closePopup() 来关闭。

注意，从 V0.8.0 版本开始，才可以可以加入 `.weui-popup-overlay `这个半透明遮罩层。