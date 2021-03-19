<template>
	<view class="Hybody">
		<view class="title">
			消息
		</view>
		<view class="content">
			<view class="box">
				<view class="boxleft">
					<view class="img">
						<image src="../../../static/tu.jpg"></image>
					</view>
					<text class="text">我购买的服务</text>
				</view>
				<view class="num">
					2
				</view>
			</view>
			<view class="box">
				<view class="boxleft">
					<view class="img">
						<image src="../../../static/tu.jpg"></image>
					</view>
					<text class="text">收藏我发布的服务</text>
				</view>
				<view class="num">
					>
				</view>
			</view>			
			<tidings :dataList="dataList"></tidings>
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

<style>
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
		padding: 20upx 32upx;
	}
	.content{
		height: 1500upx;
		line-height: 20px;
		border-radius: 45px 45px 0px 0px;
		text-align: center;
		background-color: rgb(45,46,41);
	}
	.box{
		display: flex;
		justify-content: space-between;
		align-items: center;
		padding:30upx 50upx;
	}
	.boxleft{
		display: flex;
		align-items: center;
	}
	.img{
		border-radius: 50%;
	}
	.img image{
		width:121upx ;
		height: 121upx;
		border-radius: 50%;
	}
	.text {
		margin-left: 10upx;
	}
	.num{
		width: 44upx;
		height: 44upx;
		background-color:#F36D11;
		border-radius: 50%;
	}
</style>
