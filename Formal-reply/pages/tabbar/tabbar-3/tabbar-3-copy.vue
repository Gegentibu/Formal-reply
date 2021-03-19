<template>
	<view  class="Hybody">
		<view class="fabiao">
			<image src="../../../static/fabiao.png" mode="" @click="goToFbdt"></image>
		</view>
		<view class="release">
			<view class="releaseTitle">
				活动发布
			</view>
			<view class="releaseBj" @click="goToHd">
				<text class="releaseBjTitle">让好产品走出去让更多人购买</text>
				<text class="releaseBjText">在这里您可以出售您公司或代理产品及朋友的产品来互动营销，让指尖生意源源不断的继续。</text>
			</view>
		</view>
		<view class="release">
			<view class="releaseTitle">
				咨询发布
			</view>
			<view class="releaseBj" @click="goToZx">
				<text class="releaseBjTitle">让好产品走出去让更多人购买</text>
				<text class="releaseBjText">在这里您可以出售您公司或代理产品及朋友的产品来互动营销，让指尖生意源源不断的继续。</text>
			</view>
		</view>
		<view class="release">
			<view class="releaseTitle">
				产品发布
			</view>
			<view class="releaseBj" @click="goToCp">
				<text class="releaseBjTitle">让好产品走出去让更多人购买</text>
				<text class="releaseBjText">在这里您可以出售您公司或代理产品及朋友的产品来互动营销，让指尖生意源源不断的继续。</text>
			</view>
		</view>
		<view class="release">
			<view class="releaseTitle">
				虚拟产品发布
			</view>
			<view class="releaseBj" @click="goToXncp">
				<text class="releaseBjTitle">让好产品走出去让更多人购买</text>
				<text class="releaseBjText">在这里您可以出售您公司或代理产品及朋友的产品来互动营销，让指尖生意源源不断的继续。</text>
			</view>
		</view>
		<view class="release">
			<view class="releaseTitle">
				项目发布
			</view>
			<view class="releaseBj" @click="goToXm">
				<text class="releaseBjTitle">让好产品走出去让更多人购买</text>
				<text class="releaseBjText">在这里您可以出售您公司或代理产品及朋友的产品来互动营销，让指尖生意源源不断的继续。</text>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: 'Hello'
			}
		},
		onLoad() {

		},
		methods: {
			goToFbdt(){
				uni.navigateTo({
					url: '/pages/tabbar/tabbar-3/fabiaodongtai',
				});
			},
			goToCp(){
				uni.navigateTo({
					url: '/pages/tabbar/tabbar-3/chanpinfabu',
				});
			},
			goToHd(){
				uni.navigateTo({
					url: '/pages/tabbar/tabbar-3/huodongfabu',
				});
			},
			goToSt(){
				uni.navigateTo({
					url: '/pages/tabbar/tabbar-3/shitifabu',
				});
			},
			goToXm(){
				uni.navigateTo({
					url: '/pages/tabbar/tabbar-3/xiangmufabu',
				});
			},
			goToXncp(){
				uni.navigateTo({
					url: '/pages/tabbar/tabbar-3/xunichanpinfabu',
				});
			},
			goToZx(){
				uni.navigateTo({
					url: '/pages/tabbar/tabbar-3/zixunfabu',
				});
			}
		}
	}
</script>

<style>
	.Hybody{
		padding: 0 32upx;
		height: 100%;
		font-size: 12px;
		background-color: #080808;
		color: #fff;
	}
	.fabiao{
		width: 100%;
		height: 300upx;
		display: flex;
		justify-content: center;
		align-items: center;
	}
	.fabiao image{
		height: 248upx;
		width: 248upx;
	}
	
	.releaseTitle{
		color: rgba(255, 255, 255, 100);
		font-size: 22px;
		text-align: left;
		font-weight: 600;
		font-family: 方正工业黑-标准;
		margin-top: 12upx;
		margin-bottom: 40upx;
	}
	.releaseBj{
		width: 100%;
		height: 660upx;
		background-image: url(../../../static/tu.jpg);
		border-radius: 20upx;
	}
	.releaseBjTitle{
		padding: 60% 2% 2% 2%;
		font-size: 20px;
		font-weight: 600;
		display: block;
	}
	.releaseBjText{
		padding: 0 2%;
		font-size: 18px;
		display: block;
	}
</style>
