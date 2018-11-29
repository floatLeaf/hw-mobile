**首页导航**

![](http://wonderland123.oss-cn-hangzhou.aliyuncs.com/3c4a3a06d7d9ed52dc3e9bd075135721.jpg)

```
<!-- index-nav -->
<section class="index-navs">
	<div class="nav-item" v-for="n in 2">
		<div class="item" v-for="n in 4">
			<img class="icon" src="../../assets/image/block.jpg">
			<p>模块</p>
		</div>
	</div>
</section>
```
<br />

**小标题**

![](http://wonderland123.oss-cn-hangzhou.aliyuncs.com/ecd0e5cb0e74e170787f851dc928a05d.jpg)

```
<!-- 小标题 -->
<section class="small-title">
	<div class="text">滑动板块</div>
	<div class="opt">
		更多>
	</div>
</section> 
```


**滑动板块**

![](http://wonderland123.oss-cn-hangzhou.aliyuncs.com/0d204f5e8bd3f33aaa1e46c798c21cce.jpg)

```
<!-- 滑动板块 -->
<section class="scroll-block">
	<div class="item" v-for="n in 6" :key="n">
		<img class="img" src="../../assets/image/block.jpg">
		<p class="name">精选产品介绍简介说惆怅长岑长</p>
		<p class="price">￥123</p>
	</div>
</section>
```