<template>
	<view class="">
		<image class="bank-bg" src="../../static/images/index/背景图/会员中心.png" mode=""></image>
		<cu-custom bgColor="bg-gradual-transparent text-white" :isBack="true" class="radius"><block slot="backText"></block><block slot="content">联系客服</block></cu-custom>
		<!-- <navigator class="" hover-class="none" url="../../pages/my/my" open-type="switchTab">
			<image src="../../static/images/my/商务合作_slices/返回icon.png" style="width: 12px;height: 13px;margin-top:35px;margin-left:20px;"></image>
		</navigator>
		<view class="title">
			联系客服
		</view> -->
		
		<view class="jiemian">
			<image src="../../static/images/index/707/联系客服.png" mode="widthFix" style="width: 100%;"></image>
		</view>
	</view>
</template>

<script>
	    export default {
	        components: {
	   
	        },
	        data() {
	            return {
	                  CustomBar: this.CustomBar,
	            };
	        },
	        methods: {
	    
	        }
	    }
</script>

<style lang="scss" scoped>
	.bank-bg {
			width: 100%;
			height: 100vh;
			overflow: hidden;
			position:fixed; 
			background-size: cover;
			z-index: -10;
			background-position: center bottom; 
		}
	.title {
			color: #FFFFFF;
			font-size: 18px;
			position: relative;
			top: -10%;
			left: 42%;
			display: inline-block;
		}
	.jiemian {
		padding: 5% 0% 0 0%;
	}
</style>
