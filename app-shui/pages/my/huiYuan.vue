<template>
	<view class="box">
		<view class="ss">
			 <cu-custom bgColor="bg-gradual-transparent text-white" :isBack="true"><block slot="backText"></block></cu-custom>
		
<!-- 		<cu-custom bgColor="bg-gradual-blue" :isBack="true"><block slot="backText">返回</block><block slot="content">边框阴影</block></cu-custom> -->
			<!-- <image class="ziliao-bg" src="../../static/images/index/背景图/会员中心.png" mode=""></image> -->
			<!-- <view class="header">
				<view class="image">
					<image src="../../static/images/my/会员中心_slices/头像.png" style="width: 63px;height: 63px;margin-bottom: 12px;margin-top: 80px;"></image>
				</view>
		        <p class="name">李小姐</p>
				<view class="munber">
					<text class="cuIcon-mobile text-grey li"></text>
					<text class="text-grey">1232656565</text>
				</view>
				<view class="jifen">
					<text class="text-grey">水滴积分：52656</text>
				</view>
			</view>
			<view class="footer">
				<view class="one">
					<span class="text-grey1">联系客服</span>
					<span class="text-grey1">全部订单</span>
				</view>
				<view class="two">
					<text class="text-grey1">待付款</text>
					<text class="text-grey1">购物车</text>
				</view>
				<view class="thress">
					<text class="text-grey1">待发货</text>
					<text class="text-grey1">退换货</text>
				</view>
				<view class="footh">
					<text class="text-grey1">待收货</text>
				</view>		
			</view>
			<view class="product">
				<image src="../../static/images/my/会员中心_slices/看广告按钮.png" mode="" style="width: 375px;height: 45px;"></image>
			</view>
			 -->
			
				
		
			<!-- <view class="contain">
				<image src="../../static/images/my/会员中心_slices/地球.png" style="width: 361.5px;height: 364px;"  mode=""></image>
			</view> -->
			
			
	</view>
</view>
	
</template>

<script>
	export default {
		data() {
			return {
				size: false,
				CustomBar: this.CustomBar,
			};
		},
		methods: {
			SetSize(e) {
				this.size = e.detail.value
			}
		}
	}
</script>

<style lang="scss" scoped>
	
	.box{
		width: 100%;
		overflow:hidden;
		background: url(../../static/images/index/背景图/huiyuan.png) no-repeat;
		background-size: 100%;
	}
	.ss {
		height: 815px;
	}
	.ziliao-bg {
		width: 100%;
		height: 100%;
		position:fixed; 
		background-size:100% 100%;
		z-index: -1;
	}
	.header {
		width: 110px;
		height: 150px;
		display: block;
		margin: 0 auto;
		margin-bottom: 435px;
	}
	.image {
		margin: 0 auto;
		text-align: center;
		padding-left: 22px;
	}
	.name {
		width: 50px;
		height: 13px;
		color: #FFFFFF;
		font-size: 14px;
		letter-spacing: 2px;
		text-align: center;
		margin: 0 auto;
		margin-bottom: 0px;
		margin-left: 40px;
	}
	.munber {
		// width: 100px;
		// height: 25px;
		// margin-top: 30px;
		padding-right: 15px;
		padding-left: 25px;
		// margin: auto;
		// text-align: center;
	}
	.cuIcon-mobile {
		// width: 7.5px;
		// height: 6px;
		font-size: 14px;
		color: #6A6A6A;
		margin-right: 2px;
	}
	.text-grey {
		width: 5px;
		font-size: 12px;
		color: #B0B0B0;
	}
	.jifen {
	    width: 110px;
		height: 18px;
		line-height: 20.5px;
		background-color: rgba(42, 43, 54, 0.5);
		margin: 0 auto;
		padding-left: 20px;
		padding-bottom: 10px;
		margin: 10px 0;
	}
	.contain {
		width: 361.5px;
		height: 364px;
		margin: 0 auto;
	}
	.text-grey1 {
		width: 5px;
		font-size: 12px;
		font-weight: bold;
		color: #FFFFFF;
		margin-left: 25px;
	}
	.footer {
	   width: 100%;
	   display: inline-block;
	   margin-left: 50px;
	}
	.one {
		height: 20px;
	}
	.one .text-grey1:nth-child(1) {
	   margin-right: 130px;
	}
	.two {
		height: 25px;
	}
	.two .text-grey1:nth-child(1) {
	   margin-right: 210px;
	}
	// .one .text-grey1 {
	// 	margin-left: 20px;
	// }
	.product {
		width: 380px;
		height: 47px;
		
	}
	.radius {
		width: 35px;
		height: 35px;
		background-color: rgba(255,225,225,0.3);
		border-radius: 50%;
		margin: 6px 14px;
		}
	// .footer .text-grey1:nth-child(1) {
	// 	width: 54px;
	// 	height: 12px;
	// 	position: absolute;
	// 	left: -56px;
	// 	top: 15px;
	// }
	// .footer .text-grey1:nth-child(2) {
	// 	width: 49px;
	// 	height: 12px;
	// 	position: absolute;
	// 	left: -105px;
	// 	top: 45px;
	// }
	// .footer .text-grey1:nth-child(3) {
	// 	width: 49px;
	// 	height: 12px;
	// 	position: absolute;
	// 	left: -35px;
	// 	top: 70px;
	// }
	// .footer .text-grey1:nth-child(4) {
	// 	width: 49px;
	// 	height: 12px;
	// 	position: absolute;
	// 	left: 32px;
	// 	top: 80px;
 //    }
	// .footer .text-grey1:nth-child(5) {
	// 	width: 49px;
	// 	height: 12px;
	// 	position: absolute;
	// 	left: 105px;
	// 	top: 72px;
	// }
	// .footer .text-grey1:nth-child(6) {
	// 	width: 49px;
	// 	height: 12px;
	// 	position: absolute;
	// 	left: 165px;
	// 	top: 45px;
	// }
	// .footer .text-grey1:nth-child(7) {
	// 	width: 53px;
	// 	height: 12px;
	// 	position: absolute;
	// 	left: 135px;
	// 	top: 15px;
	// }
	@import "../../colorui/icon.css";
</style>
