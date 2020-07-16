<template>
	<view class="box">

		<image class="bank-bg" src="../../static/images/index/背景图/水滴银行-04充值.png" mode=""></image>
		<cu-custom bgColor="bg-gradual-transparent text-white" :isBack="true" class="radius">
			<block slot="backText"></block>
			<block slot="content">分销中心</block>
		</cu-custom>

		<view class="">
			<view class="center">
				<view class="">
					<image src="../../static/images/bank/分销中心_slices/分销中心01.png" style="width: 380px;"></image>
				</view>
				
				<image src="../../static/images/bank/分销中心_slices/继续邀请按钮.png" mode="" style="width: 290px;height: 75px;"></image>
				<image src="../../static/images/bank/分销中心_slices/分销中心02.png" style="width: 100%;height: 85px;margin-top: 20px;"></image>
				<view class="middle">
					<view class="middle1">
						<span class="">邀请人数</span>
						<span class="">被邀人累计消费（元）</span>
					</view>
					<view class="qian">
						<span class="">251</span>
						<span class="">2510.05</span>
					</view>
				</view>
				<view class="li">
					继续邀请
				</view>
				<p class="p">您邀请的好友注册并每次消费，可获得￥20佣金</p>
			</view>
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
			fanghui() {
				uni.redirectTo({
					url: '/pages/bank/bank'
				});

			},
		}
	}
</script>

<style css scoped>
	.box {
		width: 100%;
		overflow: hidden;
	}

	.bank-bg {
		width: 100%;
		height: 100%;
		position: fixed;
		background-size: 100% 100%;
		z-index: -1;
	}

	.center {
		width: 100%;
		height: 30%;
		overflow: hidden;
		color: #FFE5E5E5;
		font-size: 14px;
		text-align: center;
		display: flex;
		flex-direction: column;
		justify-content: center;
	}

	.center image {
		position: absolute;
		top: 0;
		left: 0;
		right: 0;
		bottom: 390px;
		margin: auto;
	}

	.center image:nth-child(2) {
		position: absolute;
		top: 58%;
		left: 0;
		right: 0;
		bottom: 270px;
		margin: auto;
	}

	.center image:nth-child(3) {
		position: absolute;
		top: 70%;
		left: 0;
		right: 0;
		bottom: 270px;
		margin: auto;
	}

	.center .middle {
		position: absolute;
		top: 44%;
		left: 0;
		right: 0;
		bottom: 270px;
		margin: auto;

	}

	.center .middle .middle1 {
		margin: 0 70px;
		display: flex;
		justify-content: space-between;
	}

	.qian {
		margin: 10px 80px;
		display: flex;
		justify-content: space-between;

	}

	.qian span {
		color: #FFBB9B73;
		font-size: 24px;
	}

	.liji {
		width: 100%;
		padding: 2.5% 5% 0 5%;
		z-index: 10;

	}

	.li {
		color: #FFBB9B73;
		font-size: 18px;
		position: absolute;
		top: 58%;
		left: 40%;
		letter-spacing: 2px;
	}

	.p {
		color: #FFE5E5E5;
		position: absolute;
		top: 65%;
		left: 14%
	}

	.radius {
		width: 35px;
		height: 35px;
		background-color: rgba(255, 225, 225, 0.3);
		border-radius: 50%;
		margin: 6px 14px;
	}
</style>
