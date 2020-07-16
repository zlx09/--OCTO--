<template>
	<view class="">
		<image class="bank-bg" src="../../static/images/index/背景图/会员中心.png" mode=""></image>
		<navigator class="content" hover-class="none" url="../../pages/my/order" open-type="redirect">
			<image src="../../static/images/my/商务合作_slices/返回icon.png" style="width: 12px;height: 13px;margin-top:35px;margin-left:20px;"></image>
		</navigator>
		<view class="title">
			订单中心
		</view>
		
		<!-- <view class="nav">
			<view class="kuang">
				<image src="../../static/images/order/待发货-2_slices/待收货.png" mode="" style="width: 65.5px;height: 27px;"></image>
				<image src="../../static/images/order/待发货-2_slices/待收货.png" mode="" style="width: 65.5px;height: 27px;"></image>
				<image src="../../static/images/order/待发货-2_slices/待收货.png" mode="" style="width: 65.5px;height: 27px;"></image>
				<image src="../../static/images/order/全部_slices/全部按钮.png" mode="" style="width: 65.5px;height: 35px;"></image>
				<image src="../../static/images/order/待发货-2_slices/待收货.png" mode="" style="width: 65.5px;height: 27px;"></image>
			</view>
			<view class="zhi">
				<view class="l">
					全部
				</view>
				<view class="l">
					待付款
				</view>
				<view class="l">
					待发货
				</view>
				<view class="l">
					待收货
				</view>
				<view class="l">
					退换货
				</view>
			</view>
		</view> -->
		
		<view class="center">
			<image src="../../static/images/order/全部_slices/shouhuo.jpg" mode="widthFix" style="width: 100%;height: 900px"></image>
		</view>
		<!-- <view class="content">
		        <view style="margin-top: 20upx;">
		             <zzx-tabs :items="items" :current="current" @clickItem="onClickItem" ref="mytabs">
		             </zzx-tabs>
		        </view> 
		        <view style="margin-top: 20upx;color:#999999;font-size: 24upx;height: 260upx;">
		            <view v-show="current === 0">
		                <image src="../../static/images/index/707/订单/全部01.png" mode="" style="width: 100%;height: 244px;"></image>
						<image src="../../static/images/index/707/订单/全部03.png" mode="" style="width: 100%;height: 269.7px;"></image>
						<image src="../../static/images/index/707/订单/全部02.png" mode="" style="width: 100%;height: 269.7px;"></image>
						<image src="../../static/images/index/707/订单/全部04.png" mode="" style="width: 100%;height: 269.7px;"></image>
		            </view>
		            <view v-show="current === 1">
		                <image src="../../static/images/order/全部_slices/全部_详情.jpg" mode="" style="width: 100%;height: 1700px;"></image>
		            </view>
		            <view v-show="current === 2">
		                <image src="../../static/images/order/待发货-2_slices/待发货_详情.jpg" mode="" style="width: 100%;height: 1700px;"></image>
		            </view>
					<view v-show="current === 3">
					   
					</view>
					<view v-show="current === 4">
					   
					</view>
		        </view>
		    </view> -->
		<!-- <view class="header-bar">
			<image src="../../static/images/bank/03_slices/圆角矩形 框.png" mode="" style="width: 72.5px;height: 35px;"></image>
			<image src="../../static/images/bank/03_slices/圆角矩形 框.png" mode="" style="width: 72.5px;height: 35px;"></image>
			<image src="../../static/images/bank/03_slices/圆角矩形 框.png" mode="" style="width: 72.5px;height: 35px;"></image>
		</view> -->
		<!-- <view class="zi">
		    <span>全部</span>
			<span>未使用</span>
			<span>已使用</span>
		</view> -->
		
		<!-- <view class="">
			
		</view> -->
	</view>
</template>

<script>
	    import zzxTabs from "@/components/zzx-tabs/zzx-tabs.vue"
	    export default {
	        components: {
	            zzxTabs
	        },
	        data() {
	            return {
	                items: ['全部','代付款','待发货','待收货','退换货'],
	                current: 0,
					activeColor: '#E4BE75'
	            };
	        },
	        methods: {
	          onClickItem(e) {
	            if (this.current !== e.currentIndex) {
	                this.current = e.currentIndex;
	            }
	          }
	        }
	    }
</script>

<style lang="scss" scoped>
	.bank-bg {
			width: 100%;
			height: 100vh;
			overflow: hidden;
			position:fixed; 
			background-size: cover;
			z-index: -10;
			background-position: center bottom; 
		}
	.title {
			color: #FFFFFF;
			font-size: 16px;
			position: relative;
			top: 30%;
			left: 40%;
			display: inline-block;
		}
	.jiantou {
		padding: 5px 15px;
	}
	.fenxiao {
		width: 375px;
		padding: 12% 0% 0 0;
		z-index: 10;
		text-align: center;
		vertical-align: middle;
		margin-bottom: 20px;
	}
	.header-bar {
		text-align: center;
		vertical-align: middle;
	}
	.header-bar image {
		width: 100%;
		margin: 20px 0 20px 12px;
	}
	.zi {
		position: absolute;
		top: 10.6%;
		left: 24%;
	}
	.zi span {
		color: #FFFFFFFF;
		margin: 0px 18px 0px 0px;
		font-size: 18px;
	}
	.zi span:nth-child(2) {
		margin-left: 20px;
		color: #FFDAB689;
	}
	.zi span:nth-child(3) {
		margin-left: 16px;
	}
	.nav {
		padding-top: 5px;
		position: relative;
	}
	.nav .kuang image {
		margin: 7% 0px 3% 2.6%;
	}
	.nav .kuang image:nth-child(4) {
		margin: 0px 0px 1% 2%;
	}
	.zhi {
		width: 100%;
		position: absolute;
		top: 35%;
	}
	.l {
		color: #FFFFFF;
		font-size: 14px;
		display: inline-block;
	}
	.l:nth-child(1) {
		color: #FFFFFF;
		font-size: 14px;
		display: inline-block;
		padding-left:7%;
	}
	.l:nth-child(2) {
		color: #FFFFFF;
		font-size: 14px;
		display: inline-block;
		padding-left:11%;
	}
	.l:nth-child(3) {
		color: #FFFFFF;
		font-size: 14px;
		display: inline-block;
		padding-left:6%;
	}
	.l:nth-child(4) {
		color: #FFFFFF;
		font-size: 14px;
		display: inline-block;
		padding-left:9%;
	}
	.l:nth-child(5) {
		color: #FFFFFF;
		font-size: 14px;
		display: inline-block;
		padding-left:8%;
	}
	.center {
		padding: 5% 1% 0 1%;
	}
	.center image {
		margin-top: 0%;
	}
</style>
