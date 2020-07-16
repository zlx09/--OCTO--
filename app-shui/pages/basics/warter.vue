<template>
	
	<view class="beijin">
	<cu-custom bgColor="bg-gradual-transparent text-white" :isBack="true" class="radius"><block slot="backText"></block></cu-custom>
		<view class="ss">
			
		</view>
	</view>
</template>

<script>
</script>

<style lang="scss" scoped>
	.beijin {
		  width: 100%;
		  overflow: hidden;
		  background: url(../../static/images/warter/水商品详情3_slices/xiangqing.png) no-repeat;
		  background-size: 100%;  
	}
	.ss{
		 width: 100%;
		 height: 3890upx;
		
	}
	.radius {
		width: 35px;
		height: 35px;
		background-color: rgba(255,225,225,0.3);
		border-radius: 50%;
		margin: 6px 14px;
		}
</style>

