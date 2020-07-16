<template>
	<view class="box">
<!-- 		<cu-custom bgColor="bg-gradual-blue" :isBack="true"><block slot="backText">返回</block><block slot="content">边框阴影</block></cu-custom> -->
		<view class="shsw">
			<image class="ziliao-bg" src="../../static/images/index/背景图/person.png" mode=""></image>
		<cu-custom bgColor="bg-gradual-transparent text-white" :isBack="true" class="radius"><block slot="backText"></block><block slot="content">收货地址</block></cu-custom>
		</view>
		
	  <view class="bj">
	  	<image src="../../static/images/index/707/jiesuan.png" style="width: 372.5px;height: 373px;" mode="widthFix"></image>
		<image src="../../static/images/index/707/jiesuan2.png" style="width: 372.5px;" mode="widthFix"></image>
		<image src="../../static/images/index/707/cart2.png" style="width: 372.5px;" mode="widthFix" @click="toTiJiao"></image>
		
	  <view class="footer">
<!-- 			<image src="../../static/images/my/购物车_slices/未选中按钮.png" style="width: 18.5px;height: 18.5px;"></image> -->
			<!-- <text >全选</text>
			<text>合计：￥1389.00</text> -->
			<!-- <span>
				<image src="../../static/images/my/购物车_slices/删除icon.png" style="width: 18.5px;height: 18.5px;"></image>
			</span> -->
			
		</view>
	  </view>
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
				size: false
			};
		},
		methods: {
			SetSize(e) {
				this.size = e.detail.value
			},
			toTiJiao(){
				uni.navigateTo({
					url:"/pages/my/tijiao"
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
	.center-right {
		position: absolute;
		top: 30px;
		right: 0px;
	}
	.bj {
		width: 100%;
		overflow: hidden;
	}
	.bj image {
		position: absolute;
		top: 0;
		left: 0;
		right: 0;
		bottom: 34%;
		margin:  auto;
	}
	.bj image:nth-child(2) {
		position: absolute;
		top: 65%;
		left: 0;
		right: 0;
		bottom: 15%;
		margin:  auto;
	}
	.bj image:nth-child(3) {
		position: absolute;
		top: 90%;
		left: 0;
		right: 0;
		bottom: 0;
		margin:  auto;
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
	@import "../../colorui/main.css";
	@import "../../colorui/icon.css";
</style>
