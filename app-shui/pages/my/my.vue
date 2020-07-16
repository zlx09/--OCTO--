<template name="components">
	<view>
		<image class="mi-bg" src="../../static/images/index/背景图/mi.png" mode=""></image>
		<scroll-view scroll-y class="page">
				<block slot="content">
					<image src="/static/cjkz.png" mode="aspectFill" style="width: 240upx;height: 60upx;"></image>
				</block>
			</cu-custom>
			<view class="cu-card">
				<view class="cu-item bg-img shadow-blur" :style="[{backgroundImage:'url('+item.img+')'}]" @tap="toChild" :data-url="item.url"
				 v-for="(item,index) in list" :key="index">
				 
					<view class="cardTitle">
						<text :class="'cuIcon-' + item.cuIcon"></text>
						{{item.title}}
					</view>
				</view>
			</view>
			<view class="cu-tabbar-height"></view>
		</scroll-view>
	</view>
</template>

<script>
	export default {
		name: "components",
		data() {
			return {
				StatusBar: this.StatusBar,
				CustomBar: this.CustomBar,
				list: [{
						title: '个人中心',
						url: '../my/ziliao',
						cuIcon: 'profile'
					},
					{
						title: '我的订单',
						url: '../my/order',
						cuIcon: 'calendar'
					},
					{
						title: '购物车',
						url: '../my/cart',
						cuIcon: 'cart'
					},
					{
						title: '会员中心',
						url: '../my/huiYuan',
						cuIcon: 'present'
					},
					{
						title: '看广告赚钱',
						url: '../bank/produce',
						cuIcon: 'discoverfill'
					},
					{
						title: '联系客服',
						url: '../my/lianxi',
						cuIcon: 'dianhua'
					},
					{
						title: '商务合作',
						url: '../my/hezuo',
						cuIcon: 'friend'
					},
					{
						title: '收货地址',
						url: '../my/shouhuo',
						cuIcon: 'location'
					},
					{
						title: '我的余额',
						url: '../my/tixian',
						cuIcon: 'moneybag'
					}
				]
			};
		},
		methods: {
			toChild(e) {
				uni.navigateTo({
					url: e.currentTarget.dataset.url
				})
			},
		},
	}
</script>

<style>
	.page {
		height: 100vh;
	}
    .mi-bg {
    		width: 100%;
    		height: 100%;
    		position:fixed; 
    		background-size:100% 100%;
    		z-index: -1;
    	}
	.cardTitle {
		color: #333333;
		padding: 30upx 20upx;
		font-size: 34upx;
		position: relative;
	    border-bottom: 1px solid rgba(255,255,255,0.5);
	}
    .cu-card>.cu-item {
		background-color: rgba(255,255,255,0);
	}
	/* [class*="cuIcon-"] {
		margin-right: 10px;
		color: #96D37E;
	} */
	[class="cuIcon-profile"] {
		margin-right: 10px;
		color: gray;
	}
	[class="cuIcon-cart"] {
		margin-right: 10px;
		color: red;
	}
	[class="cuIcon-present"] {
		margin-right: 10px;
		color: #ff5500;
	}
	[class="cuIcon-discoverfill"] {
		margin-right: 10px;
		color: #ffaa00;
	}
	[class="cuIcon-friend"] {
		margin-right: 10px;
		color: blue;
	}
	[class="cuIcon-dianhua"] {
		margin-right: 10px;
		color: #55557f;
	}
	[class="cuIcon-calendar"] {
		margin-right: 10px;
		color: #00aa00;
	}
	[class="cuIcon-location"] {
		margin-right: 10px;
		color: #aaaa7f;
	}
	[class="cuIcon-moneybag"] {
		margin-right: 10px;
		color: #d60924;
	}
	/* .cardTitle::before {
		content: "";
		position: absolute;
		width: 60upx;
		height: 6upx;
		border-radius: 20upx;
		background-color: #fff;
		display: block;
		top: 60upx;
		left: 50upx;
		transform: skew(10deg, 0deg);
	} */

	/* .cardTitle::after {
		content: "";
		position: absolute;
		width: 140upx;
		border-radius: 6upx;
		height: 24upx;
		background-color: #fff;
		display: block;
		bottom: 76upx;
		left: 90upx;
		transform: skew(10deg, 0deg);
		opacity: 0.1;
	} */
</style>
