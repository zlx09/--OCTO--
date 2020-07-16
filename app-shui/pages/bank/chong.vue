<template>
	<view class="box">
        
		<image class="bank-bg" src="../../static/images/index/背景图/水滴银行-04充值.png" mode="aspectFill"></image>
		 <cu-custom bgColor="bg-gradual-transparent text-white" :isBack="true" class="radius"><block slot="backText"></block><block slot="content">充值</block></cu-custom>
		<view class="bj">
			<view class="cu-card case" :class="isCard?'no-card':''">
				<view class="cu-item shadow">
					<view class="">
			          <image src="../../static/images/index/部件截图/04充值.png" style="width: 382px;height: 432.5px;"></image>
					</view>
				</view>
			</view>
			
				<button class="cu-item shadow">
					<image src="../../static/images/bank/04充值_slices/充值按钮.png" style="width: 700px;height: 54px;" mode="aspectFit">
						<view class="li">
							立即充值
						</view>
					</image>
				</button>
			
		</view>
			
	</view>
</template>

<script>
	export default {
			data() {
				return {
					isCard: false,
					CustomBar: this.CustomBar,
				};
			},
			methods: {
				IsCard(e) {
					this.isCard = e.detail.value
				},
				fanghui(){
					uni.redirectTo({
					    url: '/pages/bank/bank'
					});
					
				},
			}
		}
</script>

<style lang="scss" scoped>
	// .box{
	// 	width: 100%;
	// 	overflow:hidden;
	// }
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
			top: 45%;
			left: 15%;
			display: inline-block;
		}
	.jiantou {
		padding: 5px 15px;
	}
	.cu-card {
		margin-top: 35px;
	}
	.cu-card:nth-child(2) {
	    width: 312.5px;
		height: 63px;
	}
	.title {
		color: #FED291;
		font-size: 22px;
		position: absolute;
		top: 8%;
		left: 45%;
	}
	.li {
		color: #FFBB9B73;
		font-size: 16px;
		position: absolute;
	    top:5px;
		left: 40%;
	}
	.cu-item {
		background-color: rgba(255, 255, 225,0.1);
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
