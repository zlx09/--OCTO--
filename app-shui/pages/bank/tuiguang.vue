<template>
<!-- 	<view class="box">
			<cu-custom bgColor="bg-gradual-transparent text-white" @click="fanghui" :isBack="true" class="radius"><block slot="backText"></block></cu-custom>
		<view class="jifen">
			<view class="center">
			   <image src="../../static/images/bank/积分商城_slices/积分商城.jpg" style="width: 750px;height: 1700px;"></image>
			</view>
		</view>
		
		
	
    </view> -->
	<view class="beijin">
		<cu-custom bgColor="bg-gradual-transparent text-white" :isBack="true" class="radius"><block slot="backText"></block><block slot="content">积分商城</block></cu-custom>
		<view class="ss">
		
			<view class="center">
			   <image src="../../static/images/bank/积分商城_slices/积分商城.jpg" style="width: 750px;height: 1750px;"></image>
			</view>
		</view>
	</view>
	
	
</template>

<script>
export default {
		data() {
			return {
				isCard: false,
			};
		},
		methods: {
			IsCard(e) {
				this.isCard = e.detail.value
			},
		}
	}
</script>

<style lang="scss" scoped>
	
	// .box{
	// 	width: 100%;
	// 	height: 100vh;
	// 	overflow:hidden;
	// 	background: url(../../static/images/index/背景图/person.png) no-repeat;
	// 	position:fixed; 
	// 	background-size:cover;
	// 	background-position: center top;  
	// 	z-index: -1;
	// }
	// .jifen {
		
	// }
	.beijin {
		  width: 100%;
		  overflow: hidden;
		  background: url(../../static/images/index/背景图/水滴银行-04充值.png) no-repeat;
		  background-size: 100%;
	}
	.ss{
		 width: 100%;
		 height: 3003upx;
		
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
		color: #FED291;
		font-size: 20px;
		position: absolute;
		top: 2.5%;
		left: 40%;
	}
	// .jifen {
	// 	width: 100%;
	// 	height: 3303upx;
	// }
	.head {
		width: 100%;
	}
	.tuo {
		width: 100%;
		padding: 0 5% 0 5%;
		// height: 800px;
		z-index: 10;
	}
	// .one {
	// 	height: 131.5px;
	// }
	.cu-card {
		border-radius: 0;
	}
	.cu-card>.cu-item[data-v-5c655a86] {
		margin: 10px 16px 0 16px;
	}
	.center {
		margin-top: 15px;
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
