**tab页底**

![](http://wonderland123.oss-cn-hangzhou.aliyuncs.com/67d011eedf217357da42e7bd160e3555.jpg)

```
<div class="tab-wrap">
		<footer> 
			<nav :class="[{'active': tabIndex == 1}]" @click="routerChange('/', 1)">  
			    <img class="tab-icon" v-show="tabIndex != 1" :src="require('assets/image/block.jpg')">
			    <img class="tab-icon" v-show="tabIndex == 1" :src="require('assets/image/block.jpg')">
			   	<p>选项</p>
			</nav> 

			<nav :class="[{'active': tabIndex == 3}]" @click="routerChange('/lessionIndex/classTry', 3)">  
			    <img class="tab-icon" v-show="tabIndex != 3" :src="require('assets/image/block.jpg')">
			    <img class="tab-icon" v-show="tabIndex == 3" :src="require('assets/image/block.jpg')">
			   	<p>选项</p>
			</nav>

			<nav :class="[{'active': tabIndex == 4}]" @click="routerChange('/activityList', 4)">  
			    <img class="tab-icon" v-show="tabIndex != 4" :src="require('assets/image/block.jpg')">
			    <img class="tab-icon" v-show="tabIndex == 4" :src="require('assets/image/block.jpg')">
			   	<p>选项</p>
			</nav> 

			<nav :class="[{'active': tabIndex == 5}]" @click="routerChange('/card', 5)">
			    <img class="tab-icon" v-show="tabIndex != 5" :src="require('assets/image/block.jpg')">
			    <img class="tab-icon" v-show="tabIndex == 5" :src="require('assets/image/block.jpg')">
			   <p>选项</p>
			</nav> 
		</footer>
	</div>
</div>
```

**css样式**
```
.tab-wrap {
	$h: 50px;
	height: $h;

	footer {
		position: fixed;
		bottom: -1px;
		width: 100%;
		height: $h;
		display: flex;
		flex-direction: row;
		justify-content: space-between;
		align-items: center;
		background: #fff;
		border-top: 1px solid #f1f1f1;
		font-size: 13px;
		z-index: 99;

		nav {
			flex: 1;
			height: 100%;
			padding: 6px 0 0;
			display: flex;
			flex-direction: column;
			justify-content: space-between;
			align-items: center;
			color: #999;

			i, .tab-icon {
				font-size: 22px;
				margin-bottom: 4px; 
				width: 22px;
				height: 22px; 
				flex-shrink: 0;
			}

			/*.tab-img {
				width: 44px;
				height: 44px;
				margin-top: -18px;
				margin-bottom: 4px;
			}*/

			&.active {
				color: $maincolor; 
			}

			p {
				font-size: 20px;
				transform: scale(.5);
				margin-top: -7px;
			}
		}
	}
}
```