####V - Distpicker

效果图展示

![](http://xscall.oss-cn-hangzhou.aliyuncs.com/decb02ecdf519ef40514919f0e5ebcb9.png?x-oss-process=image/resize,m_fill,h_768,w_432)


#####安装
```
npm install v-distpicker --save

```


#####使用
```
import VDistpicker from 'v-distpicker'

export default {
  components: { VDistpicker }
}


<v-distpicker></v-distpicker>

```

#####带默认值的
```
<v-distpicker province="广东省" city="广州市" area="海珠区"></v-distpicker>

```

#####默认是pc端， 移动端使用 
```
<v-distpicker type="mobile"></v-distpicker>
```