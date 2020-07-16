<template>
	<view class="box">
		<view class="shsw">
			<image class="ziliao-bg" src="../../static/images/index/背景图/person.png" mode=""></image>
		</view>
		 <cu-custom bgColor="bg-gradual-transparent text-white" :isBack="true"><block slot="backText" class="radius"></block><block slot="content">购物车</block></cu-custom>
		<!-- <navigator class="content" hover-class="none" url="../../pages/my/my" open-type="switchTab">
			<image src="../../static/images/my/商务合作_slices/返回icon.png" style="width: 12px;height: 13px;margin-top:35px;margin-left:20px;"></image>
		</navigator>
		<view class="title">
			购物车
		</view> -->
		
		<view class="ces" @click="toJieSuan">
			<image src="../../static/images/my/购物车_slices/cart.jpg" mode="widthFix"></image>
		</view>
	 <!-- <view class="ces">
	  	<image src="../../static/images/index/707/cart1.png" style="" mode="widthFix"></image>
		<view class="footer">
			<image src="../../static/images/my/购物车_slices/未选中按钮.png" style="width: 18.5px;height: 18.5px;"></image>
			<text >全选</text>
			<p>合计：￥1389.00</p>
			<span>
				<image src="../../static/images/my/购物车_slices/删除icon.png" style="width: 18.5px;height: 18.5px;"></image>
			</span>
		</view>
	  </view> -->
		<!-- <navigator class="jiesuan" hover-class="none" url="../../pages/my/jiesuan" open-type="redirect">
			<image src="../../static/images/index/707/cart2.png" mode="widthFix"></image>
		</navigator> -->
	<!-- <navigator class="footer" hover-class="none" url="../../pages/my/jiesuan" open-type="redirect">
	 	
	 </navigator> -->
		
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
			},
			toJieSuan(){
				uni.navigateTo({
					url:"/pages/my/jiesuan"
				})
		}
		}
	}
</script>

<style lang="scss" scoped>
	
	.box{
		width: 100%;
		overflow:hidden;
	}
	.ziliao-bg {
		width: 100%;
		height: 100%;
		position:fixed; 
		background-size:100% 100%;
		z-index: -1;
	}
	.title {
			color: #FED291;
			font-size: 16px;
			position: relative;
			top: 15%;
			left: 15%;
			display: inline-block;
		}
	.title {
		color: #ffffff;
		font-size: 20px;
		position: absolute;
		top: 3%;
		left: 40%;
	}
	.ces{
		width: 100%;
		overflow: hidden;
	}
	.ces image{
		width: 750px;
		position: absolute;
		top: 0;
		left: 0;
		right: 0;
		bottom: 2%;
		margin: 0 auto;
		margin-top: 70px;
	}
	// .footer {
	// 	width: 100%;
	// 	height: 50px;
	// 	background-color: #FFFFFF;
	// 	color: #FF222222;
	// }
	// .footer span {
	// 	color: #000000;
	// 	position: absolute;
	// 	top: 0;
	// 	z-index: 9999;
	// }
	.ces .footer {
		width: 100%;
		position: absolute;
		top: 81%;
		left: 0;
		right: 0;
		bottom: 8%;
		margin:  auto;
		
	}
	.radius {
		width: 35px;
		height: 35px;
		background-color: rgba(255,225,225,0.3);
		border-radius: 50%;
		margin: 6px 14px;
		}
	@import "../../colorui/main.css";
	@import "../../colorui/icon.css";
</style>
