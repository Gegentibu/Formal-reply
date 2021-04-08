<template>
	<view class="Hybody">
		<view class="HyFlexB"  style="margin-top:30upx;">
			<view class="titleText">
				我的答复黑卡商家中心
			</view>
			<view class="">
				<button type="default" style="color: #fff;background-color: #120DB5;border-radius: 40upx;">发布商家服务</button>
			</view>
		</view>
		<view class="release">
			<view class="releaseTitle">
			</view>
			<view class="releaseBj" @click="goToXm">
				<text class="releaseBjTitle">让好产品走出去让更多人购买</text>
				<text class="releaseBjText">在这里您可以出售您公司或代理产品及朋友的产品来互动营销，让指尖生意源源不断的继续。</text>
			</view>
		</view>
		<view class="release">
			<view class="releaseTitle">
			</view>
			<view class="releaseBj" @click="goToXm">
				<text class="releaseBjTitle">让好产品走出去让更多人购买</text>
				<text class="releaseBjText">在这里您可以出售您公司或代理产品及朋友的产品来互动营销，让指尖生意源源不断的继续。</text>
			</view>
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
		padding: 0 32upx;
		padding-top: 50upx;
		/* height: 1500upx; */
		font-size: 14px;
		background-color: #080808;
		color: #fff;
		text-align: left;
		padding-bottom: 60upx;
	}
	.HyFlexB{
		display: flex;
		justify-content: space-between;
		align-items: center;
	}
	.titleText{
		color: rgba(255, 255, 255, 100);
		font-size: 22px;
		text-align: left;
		font-weight: 600;
		font-family: 方正工业黑-标准;
		/* margin: 40upx 0; */
		left: 30upx;
		height: 80upx;
		line-height: 80upx;
		background-color: #080808;
	}
	
	.Hybody view{
		margin: 30upx 0;
	}
	.releaseTitle{
		color: rgba(255, 255, 255, 100);
		font-size: 22px;
		text-align: left;
		font-weight: 600;
		font-family: 方正工业黑-标准;
		margin-top: 12upx;
		margin-bottom: 40upx;
	}
	.releaseBj{
		width: 100%;
		height: 660upx;
		background-image: url(../../../static/tu.jpg);
		border-radius: 20upx;
	}
	.releaseBjTitle{
		padding: 60% 2% 2% 2%;
		font-size: 20px;
		font-weight: 600;
		display: block;
	}
	.releaseBjText{
		padding: 0 2%;
		font-size: 18px;
		display: block;
	}
	.zhifu{
		width: 100%;
		padding: 0 32upx;
		background-color: #28272D;
		position: fixed;
		bottom: -34upx;
		left: -32upx;
		margin:0;
		font-size: 18px;
		font-weight: 600;
		border-radius: 40upx;
	}
</style>