####rem布局

######核心代码

```
var a = document.documentElement,
    w = a.clientWidth > 750 ? 750 : a.clientWidth;
a.style.fontSize = w / 15 + 'px';

```

>为确保不同屏幕的布局一致， 屏幕宽固定15rem， 屏幕越大字体越大