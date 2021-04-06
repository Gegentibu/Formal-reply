<template>
	<view class="Hybody">
		<view class="titleText" style="margin-top:30upx;">
			审核反馈
		</view>
		<view class="" style="margin: 80upx 0 0 0;">
			<view class="content">
				<view class="nuter">
					<view :class="target==0?'active':''" @click="setIndex" data-index="0">
							审核中
					 </view>
					<view :class="target==1?'active':''" @click="setIndex" data-index="1">
							审核失败
					 </view>
					 <view :class="target==2?'active':''" @click="setIndex" data-index="2">
					 		已发布
					  </view>
				</view>
				<swiper 
				:duration="500" 
				:current="thisindex"  
				:data-index='thisindex' 
				@change="toggle"
				:style="swiperHeight"
				circular>
					<swiper-item>
						<view class="release">
							<view class="releaseBj" @click="goToXm">
								<text class="releaseBjTitle">让好产品走出去让更多人购买</text>
								<text class="releaseBjText">在这里您可以出售您公司或代理产品及朋友的产品来互动营销，让指尖生意源源不断的继续。</text>
							</view>
						</view>
					</swiper-item>
					<swiper-item>
						<view class="release">
							<view class="releaseBj" @click="goToXm">
								<text class="releaseBjTitle">让好产品走出去让更多人购买</text>
								<text class="releaseBjText">在这里您可以出售您公司或代理产品及朋友的产品来互动营销，让指尖生意源源不断的继续。</text>
							</view>
						</view>
					</swiper-item>
					<swiper-item>
						<view class="release">
							<view class="releaseBj" @click="goToXm">
								<text class="releaseBjTitle">让好产品走出去让更多人购买</text>
								<text class="releaseBjText">在这里您可以出售您公司或代理产品及朋友的产品来互动营销，让指尖生意源源不断的继续。</text>
							</view>
						</view>
					</swiper-item>
				</swiper>
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
		height: 1500upx;
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
		/* margin: 40upx 0; */
		position: fixed;
		width: 100%;
		left: 30upx;
		height: 80upx;
		line-height: 80upx;
		background-color: #080808;
		top: 0;
	}
	
	.miList{
		display: flex;
		justify-content: space-between;
		align-items: center;
		margin: 30upx 0;
		color:rgba(153, 155, 178, 100);
	}
	.tijiao{
		width: 304upx;
		height: 63upx;
		line-height: 63upx;
		border-radius: 25upx;
		background-color: rgba(149, 70, 232, 100);
		color: rgba(255, 255, 255, 100);
		font-size: 14px;
		text-align: center;
		font-family: Microsoft Yahei;
	}
	image {
		width: 250upx;
		height: 250upx;
	}
	.HyFlexC{
		display: flex;
		justify-content: center;
		align-items: center;
	}
	.nuter{
		width: 100%;
		height: 80rpx;
		line-height: 80rpx;
		display: flex;
		justify-content: space-around;
	}
	.nuter view{
		/* flex: 1; */
		/* font-size: 30rpx; */
		text-align: center;
		transition: all 0.5s ease .1s;
		/* background-color: #f0f0f0; */
		text-align: left;
		margin-right: 20upx;
		/* font-size: 16px; */
/* 		font-size: 18px;
		font-family: '方正工业黑-标准';
		font-weight: 600; */
	}
	.active{
		box-sizing: border-box;
		/* color: #007AFF; */
/* 		border-bottom: 5rpx solid #00aaff;
		background-color: #f3ffff;
		border-radius: 10rpx;
		box-shadow: 3px 3px 5px #888888; */
		font-size: 20px;
		font-family: '方正工业黑-标准';
		font-weight: 600;
		padding-bottom:5px;
		border-bottom: 2px solid #fff;
	}
/* 	swiper{
		height: 100%;
	} */
	swiper-item{
		width: 100%;
		/* overflow: hidden; */
		text-align: center;
		/* line-height: 300rpx; */
		/* background-color: red; */
	}
	.swiper-item{
		overflow-y: scroll;
		width: 99.5%;
		height: 99%;
		/* background-color: white; */
		/* height: 99%; */
		box-sizing: border-box;
		padding: 1rpx;
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
</style>