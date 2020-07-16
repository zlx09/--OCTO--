<template>
	<view class="app-container">
		<!-- <cu-custom bgColor="bg-gradual-transparent text-white" @click="fanghui" :isBack="true" class="radius"><block slot="backText"></block></cu-custom> -->
		<view>
			<image class="build-bg" src="../../static/images/index/05党建_slices/build-bg.png" mode=""></image>
		</view>
		<view class="zaiui-bar-search-title-box">
			<view class="cu-bar search bg-red fixed no-shadow">
				<view class="search-form round">
					<text class="cuIcon-search"/>
					<input @input="searchInput" :value="searchKey" :adjust-position="false" placeholder="取消" placeholder-style="padding-left:86%" type="text" confirm-type="search"/>
					<text class="cuIcon-close close-icon" v-if="search_close" @tap="closeInput"/>
				</view>
				<view class="action">
					<text class="text-write warter">我的水滴:1000</text>
				</view>
			</view>
		</view>
		
		<view class="">
		<!-- 	<view class="" style="width: 750upx;height:46upx;display: block;z-index:10"> -->
		    <scroll-view scroll-x class="nav text-center">
		     	<view class="cu-item select" :class="0==TabCur?'text-white cur':''" @tap="tabSelect" data-id="0">
		     		<text class=""></text> 全部
		     	</view>
		     	<view class="cu-item" :class="1==TabCur?'text-white cur':''" @tap="tabSelect" data-id="1">
		     		<text class=""></text> 时政要闻
		     	</view>
		     	<view class="cu-item" :class="2==TabCur?'text-white cur':''" @tap="tabSelect" data-id="2">
		     		<text class=""></text> 最新资讯
		     	</view>
				<view class="cu-item" :class="3==TabCur?'text-white cur':''" @tap="tabSelect" data-id="3">
					<text class=""></text> 文化科普
				</view>
				<view class="cu-item" :class="4==TabCur?'text-white cur':''" @tap="tabSelect" data-id="4">
					<text class=""></text> 国际资讯
				</view>
				<view class="cu-item" :class="5==TabCur?'text-white cur':''" @tap="tabSelect" data-id="5">
					<text class=""></text> 党建中心
				</view>
				<view class="cu-item" :class="6==TabCur?'text-white cur':''" @tap="tabSelect" data-id="6">
					<text class=""></text> 资讯发布
				</view>
		     </scroll-view>
           <!--  <scroll-view scroll-x class="bg-white nav">
             	<view class="flex text-center">
             		<view class="cu-item flex-sub" :class="index==TabCur?'text-orange cur':''" v-for="(item,index) in 4" :key="index" @tap="tabSelect" :data-id="index">
             			Tab{{index}}
             		</view>
             	</view>
             </scroll-view> -->
		</view>
		<!-- 轮播图 -->
		<swiper class="screen-swiper" :class="dotStyle?'square-dot':'round-dot'" :indicator-dots="true" :circular="true"
		 :autoplay="true" interval="4000" duration="500">
			<swiper-item v-for="(item,index) in swiperList" :key="index">
				<image :src="item.url" mode="aspectFill" v-if="item.type=='image'"></image>
				<video :src="item.url" autoplay loop muted :show-play-btn="false" :controls="false" objectFit="cover" v-if="item.type=='video'"></video>
			</swiper-item>
		</swiper>
		
		<view class="cu-list menu-avatar">
			<view class="cu-item">
				<view class="cu-avatar radius lg" style="background-image:url(../../static/images/index/05党建_slices/头像1.png);"></view>
				<view class="content">
					<view class="one">
						<view class="cu-tag round bg-orange sm">NEW</view>
						<view class="text-content">当特朗普遭遇无法解决的问题时，库什纳是他脑中。</view>
					</view>
					
				</view>
				
			</view>
			<view class="cu-item">
				<view class="cu-avatar radius lg" style="background-image:url(../../static/images/index/05党建_slices/头像2.png);">
				</view>
				<view class="content margin-left">
						<view class="text-content">
							当特朗普遭遇无法解决的问题时，库什纳是他脑中。
						</view>
				</view>
			</view>
			<view class="cu-item ">
				<view class="cu-avatar radius lg" style="background-image:url(../../static/images/index/05党建_slices/头像1.png);"></view>
					<view class="content margin-left">
							<view class="text-content">
								解决当特朗普遭遇无法解决的问题，库什纳是他脑中。
							</view>
					</view>
			</view>
			<view class="cu-item">
				
				<view class="">
					<view><view class="thress">当特朗普遭遇无法解决的问题时，库什纳是他脑中。</view>
					</view>
				</view>
				
			</view>
			<view class="cu-item">
				
				<view class="">
					<view>
						<view class="thress">当特朗普遭遇无法解决的问题时，库什纳是他脑中。</view>
					</view>
				</view>
				
			</view>
		</view>
		<!-- <view class="banner">
			<image src="../../static/images/index/05党建_slices/banner.jpg" style="width: 100%;display: block;" mode="widthFix"></image>
		</view> -->
		
	<!-- 	<view class="list">
			<image src="../../static/images/index/05党建_slices/list.jpg" style="width: 100%;display: block;" mode="widthFix"></image>
		</view> -->
		<!-- <view class="container">
			<view class="line-bottom">
				<image src="../../static/images/index/05党建_slices/头像1.png" style="width: 93px;height: 93px;"></image>
		
			</view>
			<view class="line-bottom">
				<image src="../../static/images/index/05党建_slices/头像2.png" style="width: 93px;height: 93px;"></image>
				
			</view>
			<view class="line-bottom">
				<image src="../../static/images/index/05党建_slices/头像1.png" style="width: 93px;height: 93px;"></image>
		
			</view>
			<view class="line-bottom z">
				当特朗普遭遇无法解决的问题时，库什纳是他脑中。
			</view>
			<view class="line-bottom z">
				当特朗普遭遇无法解决的问题时，库什纳是他脑中。
			</view>
		</view> -->
	</view>
</template>

<script>
	export default {
		data() {
			return {
				CustomBar: this.CustomBar,
				TabCur: 0,
				scrollLeft: 0,
				cardCur: 0,
				swiperList: [{
					id: 0,
					type: 'image',
					url: '../../static/images/index/05党建_slices/banner@2x.png'
				}, {
					id: 1,
					type: 'image',
					url: '../../static/images/index/05党建_slices/banner@2x.png',
				}, {
					id: 2,
					type: 'image',
					url: '../../static/images/index/05党建_slices/banner@2x.png'
				}],
				dotStyle: false,
				towerStart: 0,
				direction: ''
			}
		},
		onLoad() {
			this.TowerSwiper('swiperList');
			// 初始化towerSwiper 传已有的数组名即可
		},
		methods: {
			DotStyle(e) {
					this.dotStyle = e.detail.value
				},
				// cardSwiper
				cardSwiper(e) {
					this.cardCur = e.detail.current
				},
				// towerSwiper
				// 初始化towerSwiper
				TowerSwiper(name) {
					let list = this[name];
					for (let i = 0; i < list.length; i++) {
						list[i].zIndex = parseInt(list.length / 2) + 1 - Math.abs(i - parseInt(list.length / 2))
						list[i].mLeft = i - parseInt(list.length / 2)
					}
					this.swiperList = list
				},
			
				// towerSwiper触摸开始
				TowerStart(e) {
					this.towerStart = e.touches[0].pageX
				},
			
				// towerSwiper计算方向
				TowerMove(e) {
					this.direction = e.touches[0].pageX - this.towerStart > 0 ? 'right' : 'left'
				},
			
				// towerSwiper计算滚动
				TowerEnd(e) {
					let direction = this.direction;
					let list = this.swiperList;
					if (direction == 'right') {
						let mLeft = list[0].mLeft;
						let zIndex = list[0].zIndex;
						for (let i = 1; i < this.swiperList.length; i++) {
							this.swiperList[i - 1].mLeft = this.swiperList[i].mLeft
							this.swiperList[i - 1].zIndex = this.swiperList[i].zIndex
						}
						this.swiperList[list.length - 1].mLeft = mLeft;
						this.swiperList[list.length - 1].zIndex = zIndex;
					} else {
						let mLeft = list[list.length - 1].mLeft;
						let zIndex = list[list.length - 1].zIndex;
						for (let i = this.swiperList.length - 1; i > 0; i--) {
							this.swiperList[i].mLeft = this.swiperList[i - 1].mLeft
							this.swiperList[i].zIndex = this.swiperList[i - 1].zIndex
						}
						this.swiperList[0].mLeft = mLeft;
						this.swiperList[0].zIndex = zIndex;
					}
					this.direction = ""
					this.swiperList = this.swiperList
				},
			}
	}
</script>

<style lang="scss" scoped>
	// body {
	// 	padding: 0;
	// 	margin: 0;
	// }
	// template,view,image {
	// 	padding: 0;
	// 	margin: 0;
	// }
	.nav {
		z-index:1;
		background-color: #E6E4E7;
	}
	.build-bg {
		width: 100%;
		height: 100%;
		position:fixed; 
		background-size:100% 100%;
		z-index: -1;
	}
	.bg-red {
		background-color: #B60A01;
	}
	.tower-swiper .tower-item {
		transform: scale(calc(0.5 + var(--index) / 10));
		margin-left: calc(var(--left) * 100upx - 150upx);
		z-index: var(--index);
	}
	.screen-swiper {
		height:182.5px;
	}
	.app-container {
		padding-top: 50px;
		overflow-x: hidden;
	}
	.uni-swiper-dots .uni-swiper-dots-horizontal>.uni-swiper-dot-active {
		background-color:red;
	}
	.cu-list.menu-avatar>.cu-item[data-v-b4ac8db8] {
		background-color: transparent;
		height: 100px;
		margin: 10px 0px;
    }
    .cu-avatar.lg[data-v-b4ac8db8] {
		width: 93px;
		height: 93px;
	}
	.thress {
		width: 390px;
		height: 15px;
		text-align: center;
		font-size: 15px;
		padding-left: 20px;
	}
	.margin-left {
		margin-left: 45px;
	}
	.one {
		width: 320px;
		padding-left: 35px;
	}
	.cu-tag[data-v-b4ac8db8] {
		margin-bottom: 20px;
		margin-right: 10px;
	}
	@import "../../lib/main.css";
	@import "../../lib/icon.css";
	@import "../../lib/animation.css";
	@import "../../lib/build.css";
</style>
