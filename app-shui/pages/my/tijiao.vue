<template>
	<view class="box">
		<!-- 		<cu-custom bgColor="bg-gradual-blue" :isBack="true"><block slot="backText">返回</block><block slot="content">边框阴影</block></cu-custom> -->
		<view class="shsw">
			<image class="ziliao-bg" src="../../static/images/index/背景图/person.png" mode=""></image>
		</view>
		<cu-custom bgColor="bg-gradual-transparent text-white" :isBack="true" class="radius"><block slot="backText"></block><block slot="content">订单结算</block></cu-custom>
		<view class="bj">
			<view class="zhezhao">
				<image src="../../static/images/index/707/jiesuan.png" style="width: 380px;height: 373px;" mode="widthFix"></image>
			</view>
			<image src="../../static/images/index/707/tijiao.png" style="width: 750px;height: 320px;" mode="widthFix"></image>




			<view class="footer">

			</view>
		</view>


	</view>
</template>

<script>
	export default {
		data() {
			return {
				size: false
			};
		},
		methods: {
			SetSize(e) {
				this.size = e.detail.value
			}
		}
	}
</script>

<style lang="scss" scoped>
	.box {
		width: 100%;
		overflow: hidden;
	}

	.ziliao-bg {
		width: 100%;
		height: 100%;
		position: fixed;
		background-size: 100% 100%;
		z-index: -1;
	}
    .zhezhao {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		z-index: -1;
	}
	.center-right {
		position: absolute;
		top: 30px;
		right: 0px;
	}

	.bj {
		width: 100%;
		overflow: hidden;
	}

	@import "../../colorui/main.css";
	@import "../../colorui/icon.css";
</style>
