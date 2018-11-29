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
<br />


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
<br />


**固定板块**

![](http://wonderland123.oss-cn-hangzhou.aliyuncs.com/1ca427fd489c5c23a649e299d36b1a62.jpg)

```
<section class="fixed-block-big">
	<div class="item" v-for="n in 2" :key="n">
		<img class="img" src="../../assets/image/block.jpg">
		<p class="name">精选产品介绍简介说惆怅长岑长</p>
		<p class="price">￥123</p>
	</div>
</section>

```
<br />

**固定板块**

![](http://wonderland123.oss-cn-hangzhou.aliyuncs.com/d9c2c223b9ad8b7920a1651d50dec870.jpg)

```
<section class="fixed-block-normal">
	<div class="item" v-for="n in 3" :key="n">
		<img class="img" src="../../assets/image/block.jpg">
		<p class="name">精选产品介绍简介说惆怅长岑长</p>
		<p class="price">￥123</p>
	</div>
</section>
```
<br />


**固定板块**

![](http://wonderland123.oss-cn-hangzhou.aliyuncs.com/8c95678c5ab6448b62c1b2decb4f4f60.jpg)

```
<section class="fixed-block-small">
	<div class="item" v-for="n in 4" :key="n">
		<img class="img" src="../../assets/image/block.jpg">
		<span class="name center">精选产品介绍简介说惆怅长岑长</span>
		<span class="tip center">标签说明</span>
	</div>
</section>
```
<br />

