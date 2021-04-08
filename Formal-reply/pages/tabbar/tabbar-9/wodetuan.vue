<template>
	<view class="Hybody">
		<view class="box">
			<view class="HyFlexB">
				<view class="">
					▉  我的邀请人:无邀请人
				</view>
				<view class="" style="background-color: #787B7B;padding: 2upx 10upx;border-radius: 10upx;">
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
		<view class="" style="padding: 0 20upx;">
			<view v-for="(item,index) in dataList" :key="index">
				<view class="HyFlexB" style="margin: 30upx 0;">
					<view class="HyFlexS">
						<view class="" style="font-size: 16px;font-weight: 400;margin-right: 20upx;">
							我的01团
						</view>
						<view class="" style="color: #999999;">
							已成团
						</view>
					</view>
					<view class=""  style="color: #999999;">
						   团队贡献¥198.00
					</view>
				</view>
				<view class="HyFlexS">
					<view v-for="(i,l) in List" :key="l" >
						<image class="tuanImg" src="../../../static/tu.jpg" mode=""></image>
					</view>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	import guanzhu from '../../../component/guanzhu.vue'
	    export default {
	        components:{
	            guanzhu
	        },
	        data() {
	            return {
					dataList:[{},{},{}],
					List:[{},{},{},{},{},{},{}]
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
		height: 1500upx;
		font-size: 14px;
		background-color: #080808;
		color: #fff;
		text-align: left;
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
	.tuanImg{
		width: 80upx;
		height: 80upx;
		margin-right: 10upx;
		border-radius: 50%;
	}
</style>
