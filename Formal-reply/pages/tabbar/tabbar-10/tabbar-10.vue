<template>
	<view class="Hybody">
		<view class="tanchuang">
			<view class="" style="font-size: 16px;text-align: center;font-weight: 600;margin: 50upx 0;">
				您暂无申请资格
			</view>
			<view class="" style="margin: 40upx 0; font-size: 16px;text-indent: 2em;">
				请先开通铂金及以上会员，目前已为少数人开放，请继续努力经常使用答复，关注黑卡最近动态，拥有答复黑卡即玩转黑卡线下实体商家门店。
			</view>
			<view class="" style="margin: 40upx 0; font-size: 16px;text-indent: 2em;">
				每一个黑卡实体店铺消费都有折扣，最低至五折消费。
			</view>
			<view class="">
				<button type="default" style="color: #fff;background-color: #120DB5;border-radius: 40upx;width: 60%;">开通会员</button>
			</view>
		</view>
		<view class="HyFlexBb" style="margin-top:30upx;">
			<view class="titleText">
				答复黑卡
			</view>
			<view class="">
				答复黑卡会员是您身份的象征
			</view>
		</view>
		<view class="">
			<image style="width: 100%;" src="../../../static/logo.png" mode=""></image>
		</view>
		<view class="" style="margin: 40upx 0;">
			<button type="default" style="border-radius: 30upx;background-color: #120DB5;color: #fff;padding: 10upx 0;">申请黑卡</button>
		</view>
		<view class="" style="color: #808080;">
			申请黑卡是免费的，但首先您要成为铂金以上会员
			拥有黑卡身份后可以通过答复应用超低折扣在线上
			购买黑卡特定不断增加的线下商家产品和服务。
		</view>
	</view>
</template>

<script>
	    export default {
	        data() {
	            return {
					target:0,
					swiperHeight:'height:500px',
					thisindex:0,
					dataList:[{},{},{}],
					data:[{},{}]
	            }
	        },
	        onLoad() {
				var that = this;
				const query = uni.createSelectorQuery().in(this);
				query.select('#swiperHeight').boundingClientRect(data => {
					console.log(data.height)
					that.swiperHeight ='height:'+data.height+50+'px';
				}).exec();
	        },
	        methods: {
				toggle(e){
						let index = e.detail.current
						this.target = index
				},
				setIndex(e){
					let index = e.currentTarget.dataset.index
					this.thisindex = index
				},
	            onSelected(res){
	                console.log(res)
	            },
	            dateChange(d){
	               uni.showToast({
	                   icon:'none',
	                   title:d
	               })
	            }
	        }
	    }
</script>

<style scoped>
	.Hybody{
		padding: 0 40upx;
		padding-top: 50upx;
		height: 1500upx;
		font-size: 14px;
		background-color: #080808;
		color: #fff;
		text-align: left;
		padding-bottom: 60upx;
	}
	.HyFlexBb{
		display: flex;
		justify-content: space-between;
		align-items: flex-end;
	}
	.titleText{
		color: rgba(255, 255, 255, 100);
		font-size: 22px;
		text-align: left;
		font-weight: 600;
		font-family: 方正工业黑-标准;
	}
	.tanchuang{
		position: fixed;
		top: 300upx;
		width: 74%;
		left: 10%;
		background-color: #fff;
		color: #000000;
		border-radius: 40upx;
		padding: 40upx 3%;
		z-index: 2;
	}
</style>