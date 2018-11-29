**商品详情**

![](http://wonderland123.oss-cn-hangzhou.aliyuncs.com/e59994482ca851a73fd15ad943a739ff.jpg)


**商品信息区域**
```
<div class="goods-info" style="margin-bottom: 10px;">
	<p class="name">商品名称商品名称商品名称商品名称商品名称商品名称</p>

	<div class="price-sale">
		<div class="price">
			<div class="new">￥<span>12.00</span></div>
			<del class="old">￥12</del>
		</div>

		<div class="sale">已售1923笔</div>
	</div> 
</div>
```

**商品规格**
```
<div class="small-title">
	<div class="text">商品规格</div> 
</div>

<div class="goods-specs" style="margin-bottom: 10px;">
	<div class="spec-wrap">
		<span class="spec" v-for="n in 6">黄色</span>
	</div>
</div>
```

**数量增减**

```
<div class="goods-num">
	<span>数量</span>
	<div class="num-calculate">
		<span>-</span>
		<input type="number">
		<span>+</span>
	</div>
</div>
```

**底部商品操作**
```
<!-- 底部商品操作 -->
<div class="goods-options-wrap">
	<div class="goods-options">
		<div class="opt-normal-wrap">
			<div class="opt-normal" v-for="n in 2">
				<img class="icon" src="../../assets/image/block.jpg">
				<p class="text">电话</p>
			</div>

			<div class="opt-normal with-dot">
				<img class="icon" src="../../assets/image/block.jpg">
				<p class="text">电话</p>
				<span class="dot">2</span>
			</div>
		</div>

		<div class="opt-btn-wrap">
			<button class="btn-default">加入购物车</button>
			<button class="btn-active" disabled>立即购买</button>
		</div>
	</div>
</div>
```
