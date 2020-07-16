<template>
	<view class="box">
		<image class="bank-bg" src="../../static/images/index/背景图/水滴银行-04充值.png" mode=""></image>
			 <cu-custom bgColor="bg-gradual-transparent text-white" :isBack="true" class="radius"><block slot="backText"></block><block slot="content">优惠券</block></cu-custom>
	<!-- 	<view class="jiantou">
			<image src="../../static/images/bank/优惠券-全部_slices/返回icon.png" mode="" style="width: 11px;height: 12px;"></image>
			<view class="title">
				优惠券
			</view>
		</view> -->
		
		<view class="content">
		        <view style="margin-top: 20upx;">
		             <zzx-tabs :items="items" :current="current" @clickItem="onClickItem" ref="mytabs">
		             </zzx-tabs>
		        </view> 
		        <view style="margin-top: 20upx;color:#999999;font-size: 24upx;height: 260upx;">
		            <view v-show="current === 0">
		                <image src="../../static/images/bank/04充值_slices/优惠_全部.jpg" mode="" style="width: 100%;height: 480px;"></image>
		            </view>
		            <view v-show="current === 1">
		                 <image src="../../static/images/bank/04充值_slices/优惠券.jpg" mode="" style="width: 100%;height: 590px;"></image>
		            </view>
		            <view v-show="current === 2">
		               
		            </view>
		        </view>
		    </view>
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
	                items: ['全部','未使用','已使用'],
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
		position:fixed; 
		background-size:cover;
		background-position: center top;  
		z-index: -1;
		}
	.title {
			color: #FED291;
			font-size: 16px;
			position: relative;
			top: 25%;
			left: 42%;
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
	.radius {
		width: 35px;
		height: 35px;
		background-color: rgba(255,225,225,0.3);
		border-radius: 50%;
		margin: 6px 14px;
	}
	.l {
		display: block;
	}
</style>
