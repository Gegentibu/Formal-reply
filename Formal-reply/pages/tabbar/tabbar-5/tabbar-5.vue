<template>
	<view class="Hybody">
		<view class="title">
			<view class="guanggaoci">
				     上官希尔刚邀请了2位好友获得274元
			</view>
			<view class="name">
				上官喜儿
			</view>
			<view class="nameid">
				欢迎入住答复线上CBD中心
			</view>
			<view class="nameid">
				个人ID：997K4T
			</view>
			<view class="HyFlexB" style="padding:50upx 60upx 0 60upx;font-weight: 600;">
				<view class="HyFlexL">
					<view class="">
						<image src="../../../static/img/tabbar/homeactive.png" mode=""></image>
					</view>	
					<view class="">
						黑钻会员
					</view>	
				</view>	
				<view class="HyFlexR">
					<view class="">
						<image src="../../../static/img/tabbar/homeactive.png" mode=""></image>
					</view>	
					<view class="">
						我的主页
					</view>
				</view>	
			</view>			
		</view>
		<view class="myImg">
			<view class="myImgbox">
				<image src="../../../static/tu.jpg" mode=""></image>
			</view>
		</view>
		<view class="HyFlexB" style="padding:50upx 80upx 0 80upx;font-weight: 600;">
			<view class="HyFlexL">
				<view class="">
				</view>	
				<view class="">
					推广海报
				</view>	
			</view>	
			<view class="HyFlexR">
				<view class="">
				</view>	
				<view class="">
					我要赚钱
				</view>
			</view>	
		</view>	
		<view class="HyFlexM miaoshu">
			<view class="">
				越自律，越自由
			</view>
			<view class="">
				<image src="../../../static/img/tabbar/me.png" mode=""></image>
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

		}
	}
</script>

<style>
	.Hybody {
		/* padding: 0 32upx; */
		height: 1500upx;
		font-size: 12px;
		background-color: #080808;
		color: #fff;
	}
	.title{
		text-align: center;
		height: 360upx;
		background-color: rgba(18, 13, 181, 100);
		border-bottom-left-radius: 40px;
		border-bottom-right-radius: 40px;
	}
	
	.guanggaoci{
		height: 50upx;
		font-size: 16px;
		line-height: 50upx;
	}
	.name{
		font-family: 方正工业黑-标准;
		font-weight: 600;
		font-size: 26px;
		margin: 20upx 0;
	}
	.nameid{
		margin: 5upx 0;
		font-size: 14px;
		color: rgb(153, 155, 178);
	}
	.HyFlexB{
		display: flex;
		justify-content: space-between;
		align-items: center;
		font-size: 14px;
	}
	.HyFlexB image{
		width: 34upx;
		height: 34upx;
	}
	.HyFlexM{
		display: flex;
		justify-content: center;
		align-items: center;
	}
	.HyFlexL{
		display: flex;
		justify-content: flex-start;
		align-items: center;
	}
	.HyFlexR{
		display: flex;
		justify-content: flex-end;
		align-items: center;
	}
	.myImg{
		display: flex;
		justify-content: center;
		position: relative;
	}
	.myImgbox{
		width: 200upx;
		height: 200upx;
		display: flex;
		justify-content: center;
		border-radius: 50%;
		border: 8px solid #080808;
		position: absolute;
		top: -104upx;
	}
	.myImg image{
		width: 200upx;
		height: 200upx;
		border-radius: 50%;
	}
	.miaoshu {
		margin-top: 50upx;
	}
	.miaoshu image{
		width: 24upx;
		height: 24upx;
	}
</style>
