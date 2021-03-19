<template>
	<view class="Hybody">
		<view class="head">
			<view class="" style="margin-top: 40px;">
				<image src="../../../static/tu.jpg" mode=""></image>
			</view>
			<view class="" style="width: 100%;text-align: center;">
				系统消息
			</view>
		</view>
		<view class="" style="height: 1500upx;">
			<view class="" style="text-align: center;">
				今天 21:30
			</view>
			<view class="dfMes">
				<view class="">
					<image class="dfMesImg" src="../../../static/tu.jpg" mode=""></image>
				</view>
				<view class="messige">
					这是往期照片
				</view>
			</view>
			<view class="wdMes">
				<view class="messige">
					你好
				</view>
				<view class="">
					<image class="wdMesImg" src="../../../static/tu.jpg" mode=""></image>
				</view>
			</view>
			<view class="dfMes">
				<view class="">
					<image class="dfMesImg" src="../../../static/tu.jpg" mode=""></image>
				</view>
				<view class="messige">
					<image class="messigeImg" src="../../../static/tu.jpg" mode=""></image>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
</script>

<style>
	.Hybody{
		padding: 0 32upx;
		height: 100%;
		font-size: 12px;
		background-color: #080808;
		color: #fff;
	}
	.head{
		height: 300upx;
		background-color: rgb(62,63,59);
		border-bottom-left-radius: 80upx;
		border-bottom-right-radius: 80upx;
		display: flex;
		justify-content: center;
		align-items: flex-start;
		flex-wrap: wrap;
		margin-bottom: 30upx;
	}
	.head image{
		width: 120upx;
		height: 120upx;
		border-radius: 50%;
	}
	.dfMes{
		display: flex;
		justify-content: flex-start;
		flex-wrap: nowrap;
	}
	.wdMes{
		display: flex;
		justify-content: flex-end;
		flex-wrap: nowrap;
	}
	.wdMes .messige{
		text-align: right;
	}
	.wdMesImg,.dfMesImg{
		border-radius: 50%;
		width: 110upx;
		height: 110upx;
		margin: 0 14upx;
	}
	.messige{
		width: 470upx;
		margin-top: 20rpx;
		font-size: 14px;
	}
	.dfMes .messige .messigeImg,.wdMes .messige .messigeImg{
		max-width: 470upx;
		border-radius: 20upx;
		border: 2px solid #333333;
		
	}
</style>
