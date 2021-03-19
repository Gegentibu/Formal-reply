<template>
	<view class="Hybody">
		<view class="title">
			我购买的服务
		</view>
		<view class="" style="padding: 0 70upx;height: 1500upx;">
			<view class="fuwuList">
				<view class="pImg">
					<image src="../../../static/tu.jpg" mode=""></image>
				</view>
				<view class="" style="width: 360upx;">
					<view class="" style="    margin-bottom: 5px;">
						荔枝
					</view>
					<view class="shijianImg">
						今天 09:51 <image src="../../../static/img/tabbar/newsactive.png" mode=""></image>
					</view>
				</view>
				<view class="fuwuImg">
					<image src="../../../static/tu.jpg" mode=""></image>
				</view>
			</view>
			<view class="fuwuList">
				<view class="pImg">
					<image src="../../../static/tu.jpg" mode=""></image>
				</view>
				<view class="" style="width: 360upx;">
					<view class="" style="    margin-bottom: 5px;">
						荔枝
					</view>
					<view class="shijianImg">
						今天 09:51 <image src="../../../static/img/tabbar/newsactive.png" mode=""></image>
					</view>
				</view>
				<view class="fuwuImg">
					<image src="../../../static/tu.jpg" mode=""></image>
				</view>
			</view>
			<view class="fuwuList">
				<view class="pImg">
					<image src="../../../static/tu.jpg" mode=""></image>
				</view>
				<view class="" style="width: 360upx;">
					<view class="" style="    margin-bottom: 5px;">
						荔枝
					</view>
					<view class="shijianImg">
						今天 09:51 <image src="../../../static/img/tabbar/newsactive.png" mode=""></image>
					</view>
				</view>
				<view class="fuwuImg">
					<image src="../../../static/tu.jpg" mode=""></image>
				</view>
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

		}
	}
</script>

<style scoped>
	.Hybody {
		/* padding: 0 32upx; */
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
		padding: 30upx 32upx;
		border-bottom: 1px solid #393942;
	}
	.fuwuList{
		display: flex;
		justify-content: space-between;
		align-items: center;
		flex-wrap: wrap;
		margin: 40upx 0;
	}
	.pImg image{
			border-radius: 50%;
			width:121upx ;
			height: 121upx;
	}
	.shijianImg image{
		width: 26upx;
		height: 26upx;
		margin-left: 30upx;
	}
	.fuwuImg image{
		width:121upx ;
		height: 121upx;
		border-radius: 10upx;
	}
</style>
