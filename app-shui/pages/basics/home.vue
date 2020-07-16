<template name="basics">
	<view>
		<view class="page" @click="toWarter">
			<image class="bg" src="/static/images/index/背景图/index-bg.png"></image>
		</view>
	</view>
</template>

<script>
	export default {
		name: "basics",
		data() {
			return {

			};
		},
		methods:{
			toWarter(){
				uni.navigateTo({
					url:"/pages/basics/war"
				})
			}
		}
	}
</script>

<style>
	.page {
		 height: 100vh;
	}
	.bg {
		  width: 100%;
		  height: 100vh;
		  background-size:cover;
		  background-position: center bottom;  
		  z-index: -1;
	}
</style>
