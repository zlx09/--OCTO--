<template>
	<view>
		<basics v-if="PageCur=='basics'"></basics>
		<plugin v-if="PageCur=='plugin'"></plugin>
		<bank v-if="PageCur=='bank'"></bank>
		<my v-if="PageCur=='my'"></my>
		<view class="cu-bar tabbar bg-white foot">
			<view class="action" @click="NavChange" data-cur="basics">
				<view class='cuIcon-cu-image'>
					<image :src="'/static/tabbar/shouye' + [PageCur=='basics'?'_select':''] + '.png'"></image>
				</view>
				<view :class="PageCur=='basics'?'text-green':'text-gray'">首页</view>
			</view>
			
			<view class="action" @click="NavChange" data-cur="plugin">
				<view class='cuIcon-cu-image'>
					<image :src="'/static/tabbar/build' + [PageCur == 'plugin'?'_select':''] + '.png'"></image>
				</view>
				<view :class="PageCur=='plugin'?'text-green':'text-gray'">党建</view>
			</view>
			<view class="action" @click="NavChange" data-cur="bank">
				<view class='cuIcon-cu-image'>
					<image :src="'/static/tabbar/bank' + [PageCur == 'bank'?'_select':''] + '.png'"></image>
				</view>
				<view :class="PageCur=='bank'?'text-green':'text-gray'">水滴银行</view>
			</view>
			<view class="action" @click="NavChange" data-cur="my">
				<view class='cuIcon-cu-image'>
					<image :src="'/static/tabbar/my' + [PageCur == 'my'?'_select':''] + '.png'"></image>
				</view>
				<view :class="PageCur=='my'?'text-green':'text-gray'">我的</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
		return {
				PageCur: 'basics'
			}
		},
		methods: {
			NavChange: function(e) {
				this.PageCur = e.currentTarget.dataset.cur
			}
		}
	}
</script>

<style>
	.text-green, .line-green, .lines-green {
		color: #A8DC94;
	}
    .bg-white {
		background-color: rgba(97,98,77,0.3)
	}
	.cu-bar {
		align-items: normal;
	}
</style>
