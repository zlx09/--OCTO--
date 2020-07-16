<template name="components">
	<view>
		<scroll-view scroll-y class="page">
			<image class="food-bg" src="../../static/images/index/背景图/food-bg.png" mode="aspectFill"></image>
		<!-- 	<image src="/static/componentBg.png" mode="widthFix" class="response"></image> -->
		<view class="">
			<image class="tuo" src="../../static/images/food/五谷页面-1_slices/banner.png" mode="widthFix"></image>
		</view>
		<view class="center">
			<image class="kuang" src="../../static/images/food/五谷页面-1_slices/产品底框 小.png" style="width: 54.5px;height: 53px;"></image>
			<view class="margin-bottom">
				<image src="../../static/images/food/五谷页面-1_slices/产品图小.png" style="width: 26px;height: 34px;"></image>
			</view>
			<view class="margin-bottom">
				<image src="../../static/images/food/五谷页面-1_slices/产品图小.png" style="width: 26px;height: 34px;"></image>
			</view>
			<view class="margin-bottom">
				<image src="../../static/images/food/五谷页面-1_slices/产品图小.png" style="width: 26px;height: 34px;"></image>
			</view>
			<view class="margin-bottom">
				<image src="../../static/images/food/五谷页面-1_slices/产品图小.png" style="width: 26px;height: 34px;"></image>
			</view>
			<view class="margin-bottom">
				<text class="jian">∨</text>
			</view>
			<view class="">
				<view class="center-right">
					<image src="../../static/images/food/五谷页面-1_slices/dami.jpg" style="width: 281.5px;height: 232px;"></image>
				</view>
				<navigator class="footer" hover-class="none" url="../../pages/food/fluit" open-type="redirect">
					<image src="../../static/images/food/五谷页面-1_slices/fluit.jpg" style="width: 90px;height: 27.5px;"></image>
				</navigator>
				<navigator class="footer1" hover-class="none" url="../../pages/food/shi" open-type="redirect">
					<image src="../../static/images/food/五谷页面-1_slices/shi.jpg" style="width: 90px;height: 27.5px;"></image>
				</navigator>
				<navigator class="footer2" hover-class="none" url="../../pages/food/you" open-type="redirect">
					<image src="../../static/images/food/五谷页面-1_slices/you.jpg" style="width: 90px;height: 27.5px;"></image>
				</navigator>
			</view>
		</view>
		
			<view class="nav-list">
				<navigator hover-class='none' :url="'/pages/component/' + item.name" class="nav-li" navigateTo :class="'bg-'+item.color"
				 :style="[{animation: 'show ' + ((index+1)*0.2+1) + 's 1'}]" v-for="(item,index) in elements" :key="index">
					<!-- <view class="nav-title">{{item.title}}</view>
					<view class="nav-name">{{item.name}}</view> -->
				</navigator>
			</view>
			<view class="cu-tabbar-height"></view>
		</scroll-view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				elements: [
					{
						// title: '轮播',
						name: 'fluit',
						// color: 'olive',
						// cuIcon: 'album'
					},
					{
						// title: '轮播',
						name: 'shi',
						// color: 'olive',
						// cuIcon: 'album'
					},
					{
						// title: '轮播',
						name: 'you',
						// color: 'olive',
						// cuIcon: 'album'
					}
					
				],
			};
		}
	}
</script>

<style>
	.page {
		height: 100vh;
	}
	.food-bg {
			width: 100%;
			height: 100vh;
			overflow: hidden;
			position:fixed; 
			background-size:cover;
			background-position: center top;  
			z-index: -1;
		}
	.nav-list {
		display: flex;
		padding: 0 22px 0px;
		-webkit-box-pack:justify;
		justify-content:space-between;
		-webkit-flex-wrap:nowrap;
	}
	.nav-li {
		width: 30%;
		margin: 5% 2.5% 20px;
	}
	/* .nav-li:nth-child(2) {
		padding-left: 20px;
	} */
	.tuo {
		width: 100%;
		padding: 2.5% 5% 0 5%;
		// height: 800px;
		z-index: 10;
	}
	.center {
		position: relative;
		padding: 25px 0 0 20px;
	}
	.margin-bottom {
		margin-bottom: 20px;
		padding: 0px 13px;
	}
	.kuang {
		position: absolute;
		top: 20px;
		left: 20px;
	}
	.center-right {
		position: absolute;
		top: 30px;
		right: 0px;
	}
	.jian {
		color: #D1D0C2;
		font-size: 18px;
		position: absolute;
		top: 102%;
		left: 9%;
	}
	.footer {
		position: absolute;
		top:125%;
		left: 10%;
	}
	.footer1 {
		position: absolute;
		top:125%;
		left: 38%;
	}
	.footer2 {
		position: absolute;
		top:125%;
		left: 66%;
	}
</style>
