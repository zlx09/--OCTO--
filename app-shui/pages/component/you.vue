<template>
	<view class="beijin">
		<cu-custom bgColor="bg-gradual-transparent text-white" @click="fanghui" :isBack="true" class="radius"><block slot="backText"></block></cu-custom>
		<view class="ss">
			<navigator class="click" hover-class="none" url="../../pages/food/food" open-type="switchTab">
				<button class=""></button>
			</navigator>
			<!-- <view class="jiantou">
				<image src="../../static/images/bank/分销中心_slices/返回icon.png" mode="" style="width: 11px;height: 13px;"></image>
			</view> -->
			<view class="">
				<!-- <image src="../../static/images/warter/水商品详情3_slices/xiangqing.png" mode=""></image -->
				<!-- <view class="">
					<image src="../../static/images/warter/水商品详情3_slices/shop-bg.png" mode=""></image>
					<image src="../../static/images/warter/水商品详情3_slices/shop-bg.png" mode=""></image>
					<image src="../../static/images/warter/水商品详情3_slices/shop-bg.png" mode=""></image>
				</view> -->
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				CustomBar: this.CustomBar,
			};
		},
		methods: {
			fanghui(){
				uni.redirectTo({
				    url: '/pages/food/food'
				});
				
			},
		}
	}
</script>

<style lang="scss" scoped>
	.beijin {
		  width: 100%;
		  overflow: hidden;
		  background: url(../../static/images/food/五谷页面-1_slices/xiangqing.png) no-repeat;
		  background-size: 100%;
	}
	.ss{
		 width: 100%;
		 height: 2804upx;
		
	}
	.click {
		width: 20%;
		height: 40vh;
		// position: absolute;
		// top: 5%;
		// border:none;
		margin-top: 15px;
	}
	uni-button[plain] {
		border: none;
	}
	.jiantou {
		 padding: 5px 15px;
	}
	.radius {
		width: 40px;
		height: 40px;
		background-color: rgba(255,225,225,0.3);
		border-radius: 50%;
		margin: 4px 10px;
		}
</style>

