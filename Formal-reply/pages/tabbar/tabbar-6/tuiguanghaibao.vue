<template>
	<view class="Hybody">
		<view class="title">
			推广海报
		</view>
		<view class="haiBao">
			<view class="HyflexB" style="margin: 20upx 0;">
				<view class="">
					海报一
				</view>
				<view class="">
					<image style="width: 30upx;height: 30upx;" src="../../../static/img/tabbar/news.png" mode=""></image>
				</view>
			</view>
			<view class="">
				<image style="width: 100%;" src="../../../static/tu.jpg" mode=""></image>
			</view>
		</view>
		<view class="haiBao">
			<view class="HyflexB" style="margin: 20upx 0;">
				<view class="">
					海报一
				</view>
				<view class="">
					<image style="width: 30upx;height: 30upx;" src="../../../static/img/tabbar/news.png" mode=""></image>
				</view>
			</view>
			<view class="">
				<image style="width: 100%;" src="../../../static/tu.jpg" mode=""></image>
			</view>
		</view>
		<view class="haiBao">
			<view class="HyflexB" style="margin: 20upx 0;">
				<view class="">
					海报一
				</view>
				<view class="">
					<image style="width: 30upx;height: 30upx;" src="../../../static/img/tabbar/news.png" mode=""></image>
				</view>
			</view>
			<view class="">
				<image style="width: 100%;" src="../../../static/tu.jpg" mode=""></image>
			</view>
		</view>
	</view>
</template>

<script>
	import tidings from '../../../component/tidings.vue'
	
	export default {
		components:{
			tidings
		},
		data() {
			return {
				dataList:[{},{},{}],
				title: 'Hello'
			}
		},
		onLoad() {

		},
		methods: {
			goToGm(){
				uni.navigateTo({
					url: '/pages/tabbar/tabbar-4/goumai',
				});
			},
			goToSc(){
				uni.navigateTo({
					url: '/pages/tabbar/tabbar-4/shoucang',
				});
			},
		}
	}
</script>

<style>
	.Hybody {
		padding: 0 32upx;
		height: 100%;
		font-size: 12px;
		background-color: #080808;
		color: #fff;
	}
	.title{
		color: rgba(255, 255, 255, 100);
		font-size: 22px;
		text-align: left;
		font-weight: 600;
		font-family: 方正工业黑-标准;
		margin-bottom: 10upx;
		padding: 30upx 0;
	}
	.HyflexB{
		display: flex;
		justify-content: space-between;
		align-items: center;
	}
</style>
