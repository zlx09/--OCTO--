<template>
	<view>
		<view class="shsw">
			<image class="ziliao-bg" src="../../static/images/index/背景图/person.png" mode=""></image>
		</view>
		<cu-custom bgColor="bg-gradual-transparent text-white" :isBack="true" class="radius"><block slot="backText"></block><block slot="content">个人资料</block></cu-custom>
	<!-- 	<navigator class="content" hover-class="none" url="../../pages/my/my" open-type="switchTab">
			<image src="../../static/images/my/商务合作_slices/返回icon.png" style="width: 12px;height: 13px;margin-top:45px;margin-left:20px;"></image>
		</navigator>
		<view class="title">
			个人资料
		</view>
		<view class="padding text-center">
			<image class="ziliao-bg" src="../../static/images/my/个人资料_slices/person1.jpg" style="width: 100%;height: 389px;"></image>
		</view> -->
          
		
	  <view class="ces">
	  	<image src="../../static/images/my/个人资料_slices/person1.jpg" mode="widthFix"></image>
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
		top: 5%;
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
		bottom: 4%;
		margin:  auto;
		padding: 0 5% 0 5%;
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
