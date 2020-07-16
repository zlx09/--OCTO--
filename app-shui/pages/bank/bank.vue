<template name="bank">
	<view>
		<view class="page">
			<view class="bank-bg" src="">
			<view class="bis">
				<view class="margin-bottom" @click="tuiGuang">
					<image src="/static/images/bank/03_slices/1.jpg" style="width: 107px;height: 45px;"></image>
				</view>
				<view class="margin-bottom" @click="youHui">
					<image src="/static/images/bank/03_slices/2.jpg" style="width: 122px;height: 47px;"></image>
				</view>
				<view class="margin-bottom" @click="chongZhi">>
					<image src="/static/images/bank/03_slices/3.jpg" style="width: 104px;height: 41px;"></image>
				</view>
				<view class="margin-bottom" @click="fenXiao">
					<image src="/static/images/bank/03_slices/4.jpg" style="width: 106px;height: 43px;"></image>
				</view>
				<view class="margin-bottom" @click="produce">
					<image src="/static/images/bank/03_slices/5.jpg" style="width: 150px;height: 48px;"></image>
				</view>
			</view>
			
	
		    
		<!-- <view class="tou">
			<navigator class="tou-son" hover-class="none" url="../../pages/bank/tuiguang" open-type="redirect">
				<image src="../../static/images/bank/03_slices/1.jpg" style="width: 107px;height: 45px;"></image>
			</navigator>
			<navigator class="tou-son" hover-class="none" url="../../pages/bank/youHui" open-type="redirect">
				<image src="../../static/images/bank/03_slices/2.jpg" style="width: 118px;height: 47px;"></image>
			</navigator>
			<navigator class="tou-son" hover-class="none" url="../../pages/bank/chong" open-type="redirect">
				<image src="../../static/images/bank/03_slices/3.jpg" style="width: 106px;height: 41px;"></image>
			</navigator>
			<navigator class="tou-son" hover-class="none" url="../../pages/bank/fenXiao" open-type="redirect">
				<image src="../../static/images/bank/03_slices/4.jpg" style="width: 106px;height: 43px;"></image>
			</navigator>
			<navigator class="tou-son" hover-class="none" url="../../pages/bank/produce" open-type="redirect">
				<image src="../../static/images/bank/03_slices/5.jpg" style="width: 140px;height: 46px;"></image>
			</navigator>
		</view> -->
		</view>
	
		</view>
		
	</view>
</template>

<script>
	export default {
		name: "bank",
		data() {
			return {
			
			};
		},
		methods: {
			tuiGuang() {
				uni.navigateTo({
					url: "/pages/bank/tuiguang"
				})
			},
			youHui() {
				uni.navigateTo({
					url: "/pages/bank/youHui"
				})
			},
			chongZhi() {
				uni.navigateTo({
					url: "/pages/bank/chong"
				})
			},
			fenXiao() {
				uni.navigateTo({
					url: "/pages/bank/fenXiao"
				})
			},
			produce() {
				uni.navigateTo({
					url: "/pages/bank/produce"
				})
			},
		},
	}
</script>

<style>
	.page {
		 height: 100vh;
	}
	.bank-bg {
		  width: 100%;
		  height: 100vh;
		  background: url(../../static/images/index/背景图/bank-bg.png);
		  background-size:cover;
		  background-position: center bottom;  
		  z-index: -1;
	}
	.bis {
		width: 100%;
		height: 460px;
		display: flex;
        flex-direction: column;
		justify-content: center;
		align-items: center;
	}
	.margin-bottom {
		margin-bottom: 10px;
	}
	.margin-bottom:nth-child(5) {
		margin-top: 30px;
	}
</style>
