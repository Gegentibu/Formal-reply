<template>
	<view class="">
		<image id="logn"  @click="goToUrl('登录')" src="../../static/logn.png" mode=""></image>
	</view>
</template>

<script>
	export default {
		data() {
			return {

				}
			},
			onLoad() {
		
			},
			methods: {
				goToUrl(e){
					if(e=='登录'){
						uni.switchTab({
							url: '/pages/tabbar/tabbar-1/tabbar-1',
						});
					}
			}
		},
	}
</script>

<style>
	#logn{
			width: 100%;
			height: 1400upx;
	}
</style>
