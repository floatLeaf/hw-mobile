####fastClick插件

>用于解决click事件300ms延迟的问题和点击事件穿透的问题。但是有时会导致input难以聚焦的问题。
 

#####安装

```
npm intall fastClick --save
```
<br>

#####使用

```
import FastClick from 'fastclick'; 
if ('addEventListener' in document) {
     document.addEventListener('DOMContentLoaded', function() {
         FastClick.attach(document.body);
     }, false);
}

```

