<template>
	<view class="Hybody">
		<view class="titleText" style="margin-top:30upx;">
			答复线上CBD尊享VIP中心
		</view>
		<view class="">
				<view class="HyFlexS">
					<view class="" style="margin-right: 20upx;">
						<image style="width: 110upx;height: 110upx;border-radius: 50%;" src="../../../static/tu.jpg" mode=""></image>
					</view>
					<view class="">
						<view class="" style="font-size: 16px;font-weight: 600;margin-bottom: 20upx;">
							上官喜尔
						</view>
						<view class="" style="color: #999999;">
							您暂未开通答复VIP会员 暂无特权
						</view>
					</view>
				</view>
		</view>
		<view class="HyFlexM Hykp">
			<view class="HyFlexB wdt100">
				<view class="" style="font-size: 20px;font-weight: 400;">
					答复.尊享VIP
				</view>
				<view class="" style="font-size: 16px;">
					最低￥29.99/月
				</view>
			</view>
			<view class="HyFlexB wdt100">
				<view class="HyFlexM" style="flex-wrap: wrap;width: 65%;justify-content: start;">
					<view class="" >
						推荐开通<text style="color: #4CD964;">铂金</text>以上会员
					</view>
					<view class="" style="margin: 10upx 0;">
						推广最高每一笔奖励<text style="color: #4CD964;">275</text>元
					</view>
				</view>
				<view class="Hybtn">
					会员中心
				</view>
			</view>
		</view>
		<view class="box" style="margin-top: 10px;">
			<view class="HyFlexB">
				<view class="">
					▉  我的邀请人:无邀请人
				</view>
				<view class="" style="background-color: #787B7B;padding: 10upx 10upx;border-radius: 10upx;">
					我的团及奖励
				</view>
			</view>
			<view class="HyFlexAr">
				<view class="">
					<view class="textCenter">
						0
					</view>
					<view class="">
						会员数量
					</view>
				</view>
				<view class="">
					<view class="textCenter">
						0
					</view>
					<view class="">
						直接邀请
					</view>
				</view>
				<view class="">
					<view class="textCenter">
						0
					</view>
					<view class="">
						间接邀请
					</view>
				</view>
			</view>
		</view>
		<view class="">
			<view class="" style="font-size: 16px;text-align: center;font-weight: 400;margin: 20upx;">
				会员奖励规则
			</view>
			<view class="">
				<image style="width: 100%;" src="../../../static/奖励制度.png" mode=""></image>
			</view>
			<view class="">
				<view class="">
					邀请好友使用答复应用，开通会员，您即可获得现金奖励
				</view>
				<view class="HyFlexAr">
					<view class="" style="width: 50%;text-align: center;">
						<text style="display: block;margin: 30upx;color: red;">15%</text>
						<text style="display: block;">当前返现</text>
					</view>
					<view class=""  style="width: 50%;text-align: center;">
						<text style="display: block;margin: 30upx;color: red;">0.0</text>
						<text style="display: block;">累计收益（元）</text>
					</view>
				</view>
			</view>
		</view>
		<view class="box" style="margin-top: 20upx;">
			<view class="" style="text-align: center;">
				VIP会员邀请好友在答复订购各类有佣金的服务
			</view>
			<view class="" style="text-align: center;">
				您即可获得该产品佣金
			</view>
			<view class="">
				<button type="default" style="background-color: #120DB5;color: #fff;width: 60%;border-radius: 40upx;margin-top: 30upx;font-size: 14px;">查看佣金服务</button>
			</view>
		</view>
		<view class="" style="margin-top: 20upx;">
			<view class="">
				<text style="color: #4CD964;">▌</text>
				<text style="font-size: 16px;font-weight: 600;">如何邀请</text>
			</view>
			<view class="" style="height: 160upx;margin-top: 16upx;">
				<image style="width: 100%;height: 100%;" src="../../../static/邀请.png" mode=""></image>
			</view>
		</view>
		

	</view>
</template>

<script>
	    export default {
	        components:{
	        },
	        data() {
	            return {
					dataList:[{},{},{}],
	            }
	        },
	        onLoad() {
				
	        },
	        methods: {

	        }
	    }
</script>

<style scoped>
	.Hybody{
		padding: 0 32upx;
		padding-top: 50upx;
		height: 2000upx;
		font-size: 14px;
		background-color: #080808;
		color: #fff;
		text-align: left;
	}
	.titleText{
		color: rgba(255, 255, 255, 100);
		font-size: 22px;
		text-align: left;
		font-weight: 600;
		font-family: 方正工业黑-标准;
		margin: 40upx 0;
	}
	.HyFlexB{
		display: flex;
		justify-content: space-between;
		align-items: center;
	}
	.HyFlexAr{
		display: flex;
		justify-content: space-around;
		align-items: center;
	}
	.HyFlexS{
		display: flex;
		justify-content: start;
		align-items: center;
	}
	.box{
		background-color: #2C2D28;
		border-radius: 40upx;
		font-size: 16px;
		font-weight: 400;
		padding: 40upx;
	}
	.textCenter{
		text-align: center;
		margin: 30upx 0 10upx 0;
	}
	.Hykp{
		padding: 10upx;
		border-radius: 40upx;
		background-color: #2C2D28;
		flex-wrap: wrap;
	}
	.wdt100{
		width: 94%;
		padding: 3%;
	}
</style>
