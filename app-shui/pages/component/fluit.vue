<template>
	
	<view class="beijin">
		<cu-custom bgColor="bg-gradual-transparent text-white" @click="fanghui" :isBack="true" class="radius"><block slot="backText"></block></cu-custom>
		<view class="ss">
		
			<view class="">
			
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
		  background: url(../../static/images/food/哈密瓜详情_slices/xiangqing.png) no-repeat;
		  background-size: 100%;
	}
	.ss{
		 width: 100%;
		 height: 3003upx;
		
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

