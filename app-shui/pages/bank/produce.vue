<template>
<!-- 	<view class="box">
		<cu-custom bgColor="bg-gradual-transparent text-white" :isBack="true" class="radius"><block slot="backText"></block></cu-custom>
	
		
			<view class="cu-item shadow">
				<view class="tuo">
				 <image src="../../static/images/index/707/02.jpg" style="width: 750px;height: 131.5px;" mode="aspectFit"></image>
				</view>
			</view>
		
      <view class="cu-card case ss" :class="isCard?'no-card':''">
      	<view class="cu-item shadow">
      		<view class="">
      		<image src="../../static/images/index/707/看广告赚水滴-02.png" style="width: 385px;height: 700px;"></image>
      		</view>
      	</view>
      </view>
			
    </view> -->
	<view class="beijin">
		<cu-custom bgColor="bg-gradual-transparent text-white" :isBack="true" class="radius"><block slot="backText"></block><block slot="content">看广告赚水滴</block></cu-custom>
		<view class="ss">
		<view class="cu-item shadow">
			<view class="tuo">
			 <image src="../../static/images/index/707/02.jpg" style="width: 750px;height: 131.5px;" mode="aspectFit"></image>
			</view>
		</view>
			<view class="cu-card case ss" :class="isCard?'no-card':''">
				<view class="cu-item shadow">
					<view class="">
			           <image src="../../static/images/index/707/看广告赚水滴-02.png" style="width: 385px;height: 750px;"></image>
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
				isCard: false,
				CustomBar: this.CustomBar,
			};
		},
		methods: {
			IsCard(e) {
				this.isCard = e.detail.value
			},
		}
	}
</script>

<style lang="scss" scoped>
	
	// .box{
	// 	width: 100%;
	// 	height: 100vh;
	// 	overflow:hidden;
	// 	background: url(../../static/images/index/背景图/person.png) no-repeat;
	// 	position:fixed; 
	// 	background-size:cover;
	// 	background-position: center top;  
	// 	z-index: -1;
	// }
	// .ss{
	// 	 width: 100%;
	// 	 height: 3003upx;
		
	// }
	.beijin {
		  width: 100%;
		  // height: 100vh;
		  overflow: hidden;
		  background: url(../../static/images/index/背景图/person.png) no-repeat;
		  background-size: 100% 100%;
	}
	// .ss{
	// 	 width: 100%;
	// 	 height: 2000upx;
		
	// }
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
		left: 35%;
	}
	.head {
		width: 100%;
	}
	.tuo {
		width: 100%;
		padding: 0 5% 0 5%;
		// height: 800px;
		z-index: 10;
	}
	// .one {
	// 	height: 131.5px;
	// }
	.cu-card {
		border-radius: 0;
	}
	.cu-card>.cu-item[data-v-5c655a86] {
		margin: 10px 16px 0 16px;
	}
	.radius {
		width: 35px;
		height: 35px;
		background-color: rgba(255,225,225,0.3);
		border-radius: 50%;
		margin: 6px 14px;
	}
	// @import "../../colorui/main.css";
	// @import "../../colorui/icon.css";
</style>
