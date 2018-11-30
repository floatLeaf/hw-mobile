**活动列表页面**
![](http://wonderland123.oss-cn-hangzhou.aliyuncs.com/0276babcfac784b98934a7a68f30e7e1.jpg)

```
<section class="activity-list"> 
	<div class="list">
		<img class="goods-img" src="../../assets/image/block.jpg">
		<p class="name">活动标题活动标题活动标题活动标题活动标小星星</p>

		<section class="other-info">
			<div class="time">杭州<span>|</span>2018.07.06</div>
			<div class="price"> 
				￥<span>9.9</span>起
			</div>
		</section>
	</div>
</section>
```

**商品展示**

![](http://wonderland123.oss-cn-hangzhou.aliyuncs.com/84157adf10ef719d819092f53102aaab.jpg)

```
<section class="activity-list"> 
	<div class="list-col">
		<img class="goods-img" src="../../assets/image/block.jpg">

		<div>
			<p class="name">活动标题活动标题活动标题活动标题活动标小星星</p>

			<section class="other-info">
				<div class="time">杭州<span>|</span>2018.07.06</div>
				<div class="price"> 
					￥<span>9.9</span>起
				</div>
			</section>
		</div>
	</div>
</section>
```

![](http://wonderland123.oss-cn-hangzhou.aliyuncs.com/29623897d4a832c5e1eabd3e6fb0ebf1.jpg)

```
<div class="order-goods">
	<img class="img" src="../../assets/image/block.jpg">

	<div class="info">
		<p class="name">商品标题商品标题商品标题商品标题小星星</p>
		<p class="spec">规格：黑色</p>
		<p class="price">
			¥17.00
			<span>x1</span>
		</p>
	</div>
</div>
```	

**地址列表**

![](http://wonderland123.oss-cn-hangzhou.aliyuncs.com/504dc215fddde28f2e9563c07dc7665b.jpg)

```
<div class="address-list-wrap">
	<div class="address-list" v-for="n in 2">
		<div class="address">
			<div class="user">张小兵 <span>188****0000</span></div>
			<div class="detail">
				<span>[默认地址]</span> 浙江省杭州市江干区下沙街道福雷德广场艾肯金座  
			</div>
		</div>

		<div class="opt">
			<i class="iconfont">&#xe883;</i>
		</div>
	</div>
</div>
```

**列表展示1**

![](http://wonderland123.oss-cn-hangzhou.aliyuncs.com/0bac1dafae6784f2f9ff05bdc5cd6ebd.jpg)

```
<div class="data-lists">
	<div class="list" v-for="n in 3">
		<div class="name">商品总计</div>
		<div class="val">¥34.00</div>
	</div>
</div>
```

**表单**

![](http://wonderland123.oss-cn-hangzhou.aliyuncs.com/b65e3e43f4619c3b518e58aaf1d24c13.jpg)

```
<div class="form-wrap">
	<div class="item">
		<div class="item-name">收货人</div>
		<div class="item-val">
			<input type="text" name="" placeholder="请输入内容">
		</div>
	</div>

	<div class="item">
		<div class="item-name">收货人</div>
		<div class="item-val">
			<input type="text" name="" placeholder="请输入内容">
		</div>
		<div class="arrow"><i class="iconfont">&#xe871;</i></div>
	</div>

	<div class="item textarea">
		<div class="item-name">收货人</div>
		<div class="item-val">
			<textarea placeholder="请输入内容"></textarea>
		</div>
	</div>
</div>
````