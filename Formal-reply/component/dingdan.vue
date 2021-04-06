<template>
	<view class="dingDan">
		<view class="HyFlexB" style="flex-wrap: wrap;padding: 30upx;background-color: #3B3838;margin: 30upx 0;border-radius: 40upx;" v-for="(item,index) in dataList" :key="index" @click="goToXq">
			<view class="HyFlexB" style="width: 100%;align-items: flex-start;">
				<view class="dingDanImg">
					<image src="../static/img/release.png" mode=""></image>
				</view>
				<view class="">
					<view class="" style="text-align: right;margin-top: 20upx;">
						产品订单
					</view>
					<view class="" style="text-align: left;margin-top: 20upx;">
						呼和浩特大青山组团家庭亲子互动野营活动...
					</view>
				</view>
			</view>
			<view class="HyFlexB"  style="width: 90%;margin-left:5% ;">
				<view class="">
					￥  999.89
				</view>
				<view class="">
					有待办事件
				</view>
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
	.HyFlexB{
		display: flex;
		justify-content: space-between;
		align-items: center;
	}
	.dingDanImg image{
		width: 200upx;
		height: 200upx;
		border-radius: 20upx;
		margin: 20upx;
	}
</style>
