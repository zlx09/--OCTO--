<template>
	<view class="box">
		<cu-custom bgColor="bg-gradual-transparent text-white" :isBack="true" class="radius"><block slot="backText"></block><block slot="content">收货地址</block></cu-custom>
				<view class="cu-item">
					<view class="tuo">
						<image src="../../static/images/index/707/收货地址02-01.png" style="width: 750px;"
						 mode="widthFix"></image>
					</view>
				</view>
				
				<view class="cu-item" @click="toShouHuo3">
					<view class="two">
				      <image src="../../static/images/index/707/收货地址02.png" style="width: 750px;" mode="aspectFit"></image>
					</view>
				</view>
                
					
	</view>
</template>

<script>
	export default {
			data() {
				return {
					isCard: false
				};
			},
			methods: {
				IsCard(e) {
					this.isCard = e.detail.value
				},
				toShouHuo3(){
					uni.navigateTo({
						url:"/pages/my/shouhuo3"
					})
				}
			}
		}
</script>

<style lang="scss" scoped>
	.box {
			width: 100%;
			height: 100vh;
			overflow: hidden;
			background: url(../../static/images/index/背景图/person.png) no-repeat;
			background-size: cover;
			z-index: -10;
			background-position: center top; 
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
 @import "../../colorui/main.css";
 @import "../../colorui/icon.css";
</style>
