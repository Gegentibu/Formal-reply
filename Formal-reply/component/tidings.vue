<template>
	<view class="information">
		<view class="box" v-for="(item,index) in dataList" :key="index" @click="goToXq">
			<view class="boxleft">
				<view class="img">
					<image src="../static/logo.png" mode=""></image>
				</view>
			</view>
			<view class="boxmiddle">
				<text class="text">梦中玫瑰</text>
				<text class="text">我已收到您发来的消息</text>
			</view>
			<view class="boxright">
				<text class="text">已关注</text>
			</view>
		</view>
	</view>
</template>

<script>
	export default{
		data(){
			return{
				imgUrl:this.$imgUrl
			}
		},
		// props:["content","type"],
		props:{
			dataList:{
				type:Array
			},
		},
		methods:{
			goToXq(){
				uni.navigateTo({
					url: '/pages/tabbar/tabbar-4/xiangqing',
				});
			}
		}
	}
</script>

<style>
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
	.boxmiddle{
		width: 600upx;
		display: flex;
		height: 121upx;
		flex-wrap: wrap;
		justify-content: flex-start;
	}
	.boxright{
		width: 140upx;
		height: 121upx;
		display: flex;
		flex-wrap: wrap;
		justify-content: flex-end;
		align-items: center;
	}
	.boxright .num{
		display: flex;
		justify-content: center;
		margin-top: 10upx;
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
		width: 100%;
		display: block;
		margin-left: 10upx;
		text-align: left;
	}
	.num{
		width: 44upx;
		height: 44upx;
		background-color:#F36D11;
		border-radius: 50%;
		    margin-left: 20rpx;
	}
</style>
