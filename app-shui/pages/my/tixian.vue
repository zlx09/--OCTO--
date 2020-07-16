<template>
	<view>
		<view class="shsw">
			<image class="ziliao-bg" src="../../static/images/index/背景图/person.png" mode=""></image>
		</view>
		<cu-custom bgColor="bg-gradual-transparent text-white" :isBack="true" class="radius"><block slot="backText"></block><block slot="content">我的余额</block></cu-custom>
	<<view class="cu-item">
			<view class="tuo">
				<image src="../../static/images/index/707/tixian.jpg" style="width: 750px;"
				 mode="widthFix"></image>
			</view>
		</view>
	
	<view class="jiaoyi">
		交易记录
	</view>
	
	<view class="cu-list menu-avatar">
	<view class="cu-item">
		<view class="cu-avatar round lg" style="background-image:url(../../static/images/my/看广告赚水滴-明细_slices/记录icon.png);"></view>
		<view class="content">
			<view class="text-grey">购买驴肉土特产</view>
			<view class="text-gray text-sm flex">
				<view class="text-cut">
					2020-04-20
				</view> </view>
		</view>
		<view class="action">
			<view class="text-grey text-lg">-66.06</view>
		</view>
	</view>
  </view>
  
  <view class="cu-list menu-avatar">
  	<view class="cu-item">
  		<view class="cu-avatar round lg" style="background-image:url(../../static/images/my/看广告赚水滴-明细_slices/记录icon.png);"></view>
  		<view class="content">
  			<view class="text-grey">充值</view>
  			<view class="text-gray text-sm flex">
  				<view class="text-cut">
  					2020-04-20
  				</view> </view>
  		</view>
  		<view class="action">
  			<view class="text-red text-lg">+26</view>
  		</view>
  	</view>
  </view>
  
  <view class="cu-list menu-avatar">
  	<view class="cu-item">
  		<view class="cu-avatar round lg" style="background-image:url(../../static/images/my/看广告赚水滴-明细_slices/记录icon.png);"></view>
  		<view class="content">
  			<view class="text-grey">购买驴肉土特产</view>
  			<view class="text-gray text-sm flex">
  				<view class="text-cut">
  					2020-04-20
  				</view> </view>
  		</view>
  		<view class="action">
  			<view class="text-grey text-lg">-66.06</view>
  		</view>
  	</view>
  </view>
  
  <view class="cu-list menu-avatar">
  	<view class="cu-item">
  		<view class="cu-avatar round lg" style="background-image:url(../../static/images/my/看广告赚水滴-明细_slices/记录icon.png);"></view>
  		<view class="content">
  			<view class="text-grey">充值</view>
  			<view class="text-gray text-sm flex">
  				<view class="text-cut">
  					2020-04-20
  				</view> </view>
  		</view>
  		<view class="action">
  			<view class="text-red text-lg">+26</view>
  		</view>
  	</view>
  </view>
  
  <view class="cu-list menu-avatar">
  	<view class="cu-item">
  		<view class="cu-avatar round lg" style="background-image:url(../../static/images/my/看广告赚水滴-明细_slices/记录icon.png);"></view>
  		<view class="content">
  			<view class="text-grey">购买驴肉土特产</view>
  			<view class="text-gray text-sm flex">
  				<view class="text-cut">
  					2020-04-20
  				</view> </view>
  		</view>
  		<view class="action">
  			<view class="text-grey text-lg">-66.06</view>
  		</view>
  	</view>
  </view>
  
  <view class="cu-list menu-avatar">
  	<view class="cu-item">
  		<view class="cu-avatar round lg" style="background-image:url(../../static/images/my/看广告赚水滴-明细_slices/记录icon.png);"></view>
  		<view class="content">
  			<view class="text-grey">充值</view>
  			<view class="text-gray text-sm flex">
  				<view class="text-cut">
  					2020-04-20
  				</view> </view>
  		</view>
  		<view class="action">
  			<view class="text-red text-lg">+26</view>
  		</view>
  	</view>
  </view>
	 
	 
		
	</view>
</template>

<script>
	export default {
		data() {
			return {
				size: false,
				CustomBar: this.CustomBar,
			};
		},
		methods: {
			SetSize(e) {
				this.size = e.detail.value
			},
			// fanghui(){
			// 	uni.switchTab({
			// 	    url: '/pages/my/my'
			// 	});
				
			// },
		}
	}
</script>

<style lang="scss" scoped>
	.ziliao-bg {
		width: 100%;
		height: 100%;
		position:fixed; 
		background-size:100% 100%;
		z-index: -1;
	}
	.jiaoyi {
		color: #54837C;
		font-weight: bold;
		padding: 5% 5%;
	}
	.tuo {
		width: 100%;
		padding: 6% 3% 0 3%;
		// height: 800px;
		z-index: 10;
	}
	.two {
		margin-top: -60px;
		padding: 0% 3% 0 3%;
	}
	.cu-list.menu-avatar>.cu-item {
		background-color: transparent;
		height: 60px;
		padding: 0% 5% 0 5%;
	}
	@import "../../colorui/main.css";
	@import "../../colorui/icon.css";
</style>
