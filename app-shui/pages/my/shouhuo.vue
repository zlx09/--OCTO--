<template>
	<view>
		<view class="shsw">
			<image class="ziliao-bg" src="../../static/images/index/背景图/person.png" mode=""></image>
		</view>
		<cu-custom bgColor="bg-gradual-transparent text-white" :isBack="true" class="radius"><block slot="backText"></block><block slot="content">收货地址</block></cu-custom>
	<!-- 	<navigator class="content" hover-class="none" url="../../pages/my/my" open-type="switchTab">
			<image src="../../static/images/my/商务合作_slices/返回icon.png" style="width: 12px;height: 13px;margin-top:45px;margin-left:20px;"></image>
		</navigator>
		<view class="title">
			个人资料
		</view>
		<view class="padding text-center">
			<image class="ziliao-bg" src="../../static/images/my/个人资料_slices/person1.jpg" style="width: 100%;height: 389px;"></image>
		</view> -->
          
		
	  <view class="cu-item">
	  	<view class="tuo">
	  		<image src="../../static/images/index/707/收货地址.png" style="width: 750px;"
	  		 mode="widthFix"></image>
	  	</view>
	  </view>
	  
	  <view class="cu-item">
	  	<view class="two" @click="toShouHuo2">
	        <image src="../../static/images/index/707/收货地址01.png" style="width: 750px;" mode="aspectFit"></image>
	  	</view>
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
			},
			toShouHuo2(){
				uni.navigateTo({
					url:"/pages/my/shouhuo2"
				})
			}
			// fanghui(){
			// 	uni.switchTab({
			// 	    url: '/pages/my/my'
			// 	});
				
			// },
		}
	}
</script>

<style lang="scss" scoped>
	.ziliao-bg {
		width: 100%;
		height: 100%;
		position:fixed; 
		background-size:100% 100%;
		z-index: -1;
	}
	.tuo {
			width: 100%;
			padding: 10% 0 0 0;
			// height: 800px;
			z-index: 10;
		}
		.two {
			margin-top: -60px;
			padding: 0% 3% 0 3%;
		}
	// .radius {
	// 	width: 35px;
	// 	height: 35px;
	// 	background-color: rgba(255,225,225,0.3);
	// 	border-radius: 50%;
	// 	margin: 6px 14px;
	// }
	@import "../../colorui/main.css";
	@import "../../colorui/icon.css";
</style>
