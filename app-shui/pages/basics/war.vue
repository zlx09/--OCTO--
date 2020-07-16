<template>
	<view class="beijin">
		<cu-custom bgColor="bg-gradual-transparent text-white" :isBack="true" class="radius">
			<block slot="backText"></block>
		</cu-custom>
		<!-- <navigator class="content" url="../../pages/index/index" open-type="switchTab">
			<image src="../../static/images/bank/分销中心_slices/返回icon.png" mode="" style="width: 11px;height: 13px;"></image>
		</navigator> -->

		<view class="header">
			<p>瓶装水>></p>
			<p>桶装水>></p>
			<p>套装>></p>
		</view>
		<view class="center">
			<view class="left">
				<!-- <view class="left-one">
						<image class="kuang" src="../../static/images/warter/warter_slices/shop.png" style="width: 60px;height: 60px;"></image>
					</view> -->
				<view class="margin-bottom">
					<image src="../../static/images/warter/warter_slices/上按钮.png" style="width: 16px;height: 13px;"></image>
				</view>
				<view class="margin-bottom left-c">
					<view class="left-one">
						<view class="di">
							<image src="../../static/images/warter/warter_slices/tong.png" style="width: 22px;height: 40.5px;"></image>
						</view>

					</view>
				</view>
				<view class="margin-bottom">
					<image src="../../static/images/warter/warter_slices/tong.png" style="width: 22px;height: 40.5px;"></image>
				</view>
				<view class="margin-bottom">
					<image src="../../static/images/warter/warter_slices/tong.png" style="width: 22px;height: 40.5px;"></image>
				</view>
				<view class="margin-bottom">
					<image src="../../static/images/warter/warter_slices/tong.png" style="width: 22px;height: 40.5px;"></image>
				</view>
				<view class="margin-bottom">
					<image src="../../static/images/warter/warter_slices/商品下按钮.png" style="width: 15px;height: 12px;"></image>
				</view>
			</view>
			
			<view class="right">

				<view class="center-right">
					<view class="next">
						<view class="tong1">
							<image src="../../static/images/warter/warter_slices/tong.png" style="width: 86px;height: 157.5px;"></image>
						</view>
						<view class="yuDing" @click="toWarterXiang">
							<image src="../../static/images/warter/warter_slices/live.png" style="width: 220px;height: 90px;"></image>
						</view>
					</view>

				</view>
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
			toWarterXiang(){
				uni.navigateTo({
					url:'/pages/basics/warter'
				})
			}

		}
	}
</script>

<style lang="scss" scoped>
	.beijin {
		width: 100%;
		height: 100vh;
		overflow: hidden;
		background: url(../../static/images/index/背景图/warter.png) no-repeat;
		background-size: cover;
		z-index: -10;
		background-position: center top;
	}

	.center {
		width: 100%;
		position: absolute;
		bottom: 5px;
		display: flex;
	}

	.left {
		width: 20%;
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		z-index: 999;
	}

	.left-one {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		width: 57px;
		height: 55.5px;
		background-color: rgba(59, 63, 55, 0.5);
		border-radius: 10px;
	}

	.right {
		width: 80%;
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
        overflow: hidden;
	}

	.center-right {
		width: 640px;
		height: 242.5px;
		background: url(/static/images/warter/warter_slices/shop1.png);
		position: relative;
		display: flex;
		flex-direction: column;
		justify-content: center;
	}

	.margin-bottom {
		margin-bottom: 20px;
		padding: 0px 13px;
	}

	.kuang {
		position: absolute;
		top: 58px;
		left: 25px;
	}

	.tong {
		position: absolute;
		top: 20%;
		right: -200px;
	}

	.quan-left {
		position: absolute;
		top: 115px;
		right: -90px;
	}

	.quan-left image:nth-child(2) {
		position: absolute;
		top: 7px;
		right: 10px;
	}

	.quan-right {
		position: absolute;
		top: 115px;
		right: -250px;
	}

	.quan-right image:nth-child(2) {
		position: absolute;
		top: 7px;
		right: 8px;
	}

	.next {
		height: 400px;
		width: 640px;
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
	}

	.yuDing {
		margin:10px 0 40px 0;
	}

	.header {
		color: #FFFFFF;
		float: right;
		font-size: 18.92px;
	}

	.header p {
		margin: 40px auto;
	}

	.radius {
		width: 35px;
		height: 35px;
		background-color: rgba(255, 225, 225, 0.3);
		border-radius: 50%;
		margin: 6px 14px;
	}
</style>
