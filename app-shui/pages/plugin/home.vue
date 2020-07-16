<template name="plugin">
	<view class="">
		<view class="build-bg">
		 <view class="all">
		 	
		
		<view class="zaiui-bar-search-title-box">
			<view class="cu-bar search bg-red fixed no-shadow">
				<view class="search-form round">
					<text class="cuIcon-search"/>
					<input :adjust-position="false" placeholder="取消" placeholder-style="padding-left:86%" type="text" confirm-type="search"/>
					<text class="cuIcon-close close-icon" v-if="search_close"/>
				</view>
				<view class="action">
					<text class="text-write warter">我的水滴:1000</text>
				</view>
			</view>
		</view>
		<view class="nav">
			<image src="../../static/images/index/05党建_slices/nav.png" style="width: 750px;height: 47px;" mode=""></image>
		</view>
	
		<swiper class="screen-swiper" :class="dotStyle?'square-dot':'round-dot'" :indicator-dots="flase" :circular="true"
		 :autoplay="true" interval="4000" duration="500">
			<swiper-item v-for="(item,index) in swiperList" :key="index">
				<image :src="item.url" mode="aspectFill" v-if="item.type=='image'"></image>
				<video :src="item.url" autoplay loop muted :show-play-btn="false" :controls="false" objectFit="cover" v-if="item.type=='video'"></video>
			</swiper-item>
		</swiper>
		
		<!-- <view class="">
			<view class="">
				<image src="../../static/images/index/05党建_slices/one.png" mode="aspectFit" style="width: 100%;"></image>
			</view>
			
			<view class="">
			   <image src="../../static/images/index/05党建_slices/two.png" mode="aspectFit" style="width: 100%;"></image>
			</view>
			
			<view class="">
				<image src="../../static/images/index/05党建_slices/tress.png" mode="aspectFit" style="width: 100%;"></image>
			</view>
			<view class="cu-item">
				
				<view class="">
					<view>
						<view class="thress">当特朗普遭遇无法解决的问题时，库什纳是他脑中。</view>
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
		</view> -->
		 </view>
		</view>
	</view>
</template>

<script>
	export default {
		name:"plugin",
		data() {
			return {
				cardCur: 0,
				swiperList: [{
					id: 0,
					type: 'image',
					url: '../../static/images/index/05党建_slices/banner.png'
				}, {
					id: 1,
					type: 'image',
					url: '../../static/images/index/05党建_slices/banner.png',
				}, {
					id: 2,
					type: 'image',
					url: '../../static/images/index/05党建_slices/banner.png'
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
	.nav {
		z-index:1;
		background-color: #E6E4E7;
	}
	.build-bg {
		width: 100%;
		height: 100vh;
		background: url(/static/images/index/05党建_slices/build-bg.png) no-repeat;
		background-size:cover;
		z-index: -1;
	}
	.all {
		width: 100%;
		height: 400px;
		// background-color: blue;
		display: flex;
		flex-direction: column;
		justify-content: center;
	}
	.nav {
		
	}
	// .text-white[data-v-1c2ac8d2], .line-white[data-v-1c2ac8d2], .lines-white[data-v-1c2ac8d2] {
	// 	color: #B60A01;
	// }
	// .nav .cu-item {
	// 	padding: 0;
	// }
	// .tower-swiper .tower-item {
	// 	transform: scale(calc(0.5 + var(--index) / 10));
	// 	margin-left: calc(var(--left) * 100upx - 150upx);
	// 	z-index: var(--index);
	// }
	// .screen-swiper {
	// 	height:182.5px;
	// }
	// .app-container {
	// 	padding-top: 46px;
	// 	// overflow-x: hidden;
	// }
	// .cu-list.menu-avatar>.cu-item[data-v-1c2ac8d2] {
	// 	height: 110px;
	// 	display: flex;
	// 	flex-direction: row;
	// 	justify-content: center;
	// 	align-items: center;
 //    }
	// .left {
	// 	width: 30%;
	// 	display: flex;
	// 	flex-direction: row;
	// 	justify-content: center;
	// }
	
	// .right {
	// 	width: 70%;
		
	// }
	// .content {
	// 	width: 80%;
	// 	display: flex;
	// 	flex-direction: row;
	// 	justify-content: center;
	// 	background-color: pink;
	// }
	// .thress {
	// 	width: 390px;
	// 	height: 15px;
	// 	text-align: center;
	// 	font-size: 15px;
	// 	padding-left: 20px;
	// }
	// .one {
	// 	width: 100%;
	// 	height: 90px;
	// 	// background-color: blue;
	// 	display: flex;
	// 	flex-direction: row;
	// 	font-size: 15px;
	// }
	// .cu-tag {
	// 	margin-right: 6px;
	// }
	// .cu-tag[data-v-b4ac8db8] {
	// 	margin-bottom: 20px;
	// 	margin-right: 10px;
	// }
	@import "../../colorui/main.css";
	@import "../../colorui/animation.css";
	@import "../../colorui/build.css";
</style>
