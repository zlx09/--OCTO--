<template>
	<view>
		<view class="bank-bg">
		<cu-custom bgColor="bg-gradual-transparent text-white" :isBack="true" class="radius"><block slot="backText"></block><block slot="content">订单中心</block></cu-custom>
		
		<view class="nav">
			<view class="one">
				<view class="all">
				    全部
				</view>
			</view>
			
			<view class="two" @click="toFuKuan">
				<view class="stall">
					待付款
				</view>
			</view>
			
			<view class="three" @click="toFaHuo">
				<view class="fahuo" >
					待发货
				</view>
			</view>
			
			<view class="footh" @click="toShouHuo">
				<view class="shouhuo">
					待收货
				</view>
			</view>
			
			<view class="fine" @click="toTuiHuo">
				<view class="tuihuo">
					退换货
				</view>
			</view>
		</view>
		
		<view class="center">
			<image src="../../static/images/index/707/订单/全部01.png" mode="" style="width: 100%;height: 248px;"></image>
			<image src="../../static/images/index/707/订单/全部03.png" mode="" style="width: 100%;height: 269.7px;"></image>
			<image src="../../static/images/index/707/订单/全部02.png" mode="" style="width: 100%;height: 269.7px;"></image>
			<image src="../../static/images/index/707/订单/全部04.png" mode="" style="width: 100%;height: 250px;"></image>
		</view>
		</view>
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
					CustomBar: this.CustomBar,
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
	          },
			  toFuKuan() {
			  	uni.navigateTo({
			  		url: "/pages/my/fukuan"
			  	})
			  },
			  toFaHuo() {
			  	uni.navigateTo({
			  		url: "/pages/my/fahuo"
			  	})
			  },
			  toShouHuo() {
			  	uni.navigateTo({
			  		url: "/pages/my/shouhuo"
			  	})
			  },
			  toTuiHuo() {
			  	uni.navigateTo({
			  		url: "/pages/my/tuihuo"
			  	})
			  }
	        }
	    }
</script>

<style lang="scss" scoped>
	.bank-bg {
			width: 100%;
			background: url(/static/images/index/背景图/person.png) no-repeat;
			background-size: cover;
			z-index: -1;
			background-position: center bottom; 
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
	.nav {
		width: 100%;
		height: 60px;
		display: flex;
		flex-direction: row;
		justify-content: center;
		align-items: center;
		text-align: center;
		color: #ffffff;
	}
	
	.one {
		width: 20%;
		display: flex;
		flex-direction: row;
		justify-content: center;
		align-items: center;
		color: #B99B73;
	}
	.two {
		width: 20%;
		display: flex;
		flex-direction: row;
		justify-content: center;
		align-items: center;
	}
	.three {
		width: 20%;
		display: flex;
		flex-direction: row;
		justify-content: center;
		align-items: center;
	}
	.footh {
		width: 20%;
	    display: flex;
	    flex-direction: row;
	    justify-content: center;
	    align-items: center;
	}
	.fine {
		width: 20%;
		display: flex;
		flex-direction: row;
		justify-content: center;
		align-items: center;
	}
	
	.all {
		width: 70px;
		height: 35px;
		margin-left:10px;
		margin-top: 6px;
		background: url(/static/images/order/全部_slices/全部按钮.png) no-repeat;
	}
	.stall {
		width: 70px;
		height: 27px;
		background: url(/static/images/order/待发货-2_slices/待收货.png) no-repeat;
	}
	.fahuo {
		width: 70px;
		height: 27px;
		background: url(/static/images/order/待发货-2_slices/待收货.png) no-repeat;
	}
	.shouhuo {
		width: 70px;
		height: 27px;
		background: url(/static/images/order/待发货-2_slices/待收货.png) no-repeat;
	}
	.tuihuo {
		width: 70px;
		height: 27px;
		margin-right: 10px;
		background: url(/static/images/order/待发货-2_slices/待收货.png) no-repeat;
	}
	// .nav {
	// 	padding-top: 5px;
	// 	position: relative;
	// }
	// .nav .kuang image {
	// 	margin: 3% 0px 5% 2.7%;
	// }
	// .nav .kuang image:nth-child(1) {
	// 	margin: 0px 0px 3% 2%;
	// }
	.zhi {
		width: 100%;
		position: absolute;
		top: 19%;
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
		padding-left:8%;
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
		padding: 0 3%;
	}
	.center image {
		margin-top: 2%;
	}
</style>
