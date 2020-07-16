<template>
	<view class="box">
		<image class="bank-bg" src="../../static/images/index/背景图/水滴银行-04充值.png" mode="aspectFill"></image>
		<navigator class="content" hover-class="none" url="../../pages/bank/produce" open-type="redirect">
			<image src="../../static/images/bank/分销中心_slices/返回icon.png" style="width: 12px;height: 13px;margin-top:50px;margin-left:20px;"></image>
		</navigator>
		<view class="title">
			水滴明细
		</view>
			<view class="ces">
				<image src="../../static/images/index/707/看广告赚水滴-明细.png" mode="aspectFit"></image>
			</view>
	</view>
</template>

<script>
	export default {
			data() {
				return {
				
				};
			},
			methods: {
				
			}
		}
</script>

<style lang="scss" scoped>
	.box{
		width: 100%;
		overflow:hidden;
	}
	.bank-bg {
		width: 100%;
		height: 100vh;
		position:fixed; 
		background-size:cover;
		background-position: center top;  
		z-index: -1;
		}
	.title {
			color: #FED291;
			font-size: 16px;
			position: relative;
			top: 15%;
			left: 42%;
			display: inline-block;
		}
	.jiantou {
		padding: 5px 15px;
	}
	.title {
		color: #FED291;
		font-size: 22px;
	}
	.ces{
		width: 100%;
		overflow: hidden;
	}
	.ces image{
		position: absolute;
		top: 0;
		left: 0;
		right: 0;
		bottom: 0;
		margin:  auto;
	}
	// .cu-item {
	// 	background-color: rgba(255, 255, 225,0.1);
	// }
		@import "../../colorui/main.css";
</style>
