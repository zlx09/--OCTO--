<template>
	<view class="box">
	<!-- 	<cu-custom bgColor="bg-gradual-pink" :isBack="true"><block slot="backText">返回</block><block slot="content">卡片</block></cu-custom> -->
		<view class="shsw">
			<image class="ziliao-bg" src="../../static/images/index/背景图/person.png" mode=""></image>
		</view>
		
	<cu-custom bgColor="bg-gradual-transparent text-white" :isBack="true" class="radius"><block slot="backText"></block><block slot="content">申请退货</block></cu-custom>
	<!-- 	<view class="padding text-center">
			<image class="ziliao-bg" src="../../static/images/my/个人资料_slices/person1.jpg" style="width: 100%;height: 389px;"></image>
		</view> -->
          
		
	  <view class="ces">
	  	<image src="../../static/images/index/707/订单/全部-申请退换.png" mode="widthFix"></image>
	  </view>
	  
	  
		
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
		margin:  auto;
		padding: 0 5% 0 5%;
	}
	
	@import "../../colorui/main.css";
	@import "../../colorui/icon.css";
</style>
