<template>
	<view class="Hybody">
		<view class="" style="border-bottom: 2px solid #555555;">
			<view class="HyFlexB">
				<view class="HyFlexS">
					<view class="" style="margin-right: 20upx;">
						<image style="width: 110upx;height: 110upx;border-radius: 50%;" src="../../../static/tu.jpg" mode=""></image>
					</view>
					<view class="">
						<view class="" style="font-size: 16px;font-weight: 600;margin-bottom: 20upx;">
							Hello, Evelyn
						</view>
						<view class="" style="color: #999999;">
							6473人浏览   1359人收藏
						</view>
					</view>
				</view>
				<view class="">
					<image style="width: 70upx;height: 70upx;" src="../../../static/img/tabbar/news.png" mode=""></image>
				</view>
			</view>
			<view class="" style="margin: 30upx 0">
				昔望号：11987300
			</view>
			<view class="HyFlexS">
				<view class="HyFlexS">
					<image style="width: 36upx;height: 36upx;" src="../../../static/img/tabbar/news.png" mode=""></image>
				</view>
				<text style="margin: 0 10upx;">女</text>
				<text>内蒙古 呼和浩特</text>
				<text style="margin: 0 10upx;">6.5KM</text>
			</view>
			<view class="" style="margin: 30upx 0">
				<text style="margin-right: 10upx;">格言</text>
				<text>人生即是不断的得到和失去的过程，我们要舍得！ </text>
			</view>
			<view class="" style="margin: 30upx 0">
				<text style="margin-right: 10upx;">标签</text>
				<text class="btn">英语老师</text>
				<text class="btn" style="margin:0 30upx ">普通达人</text>
				<text class="btn" style="color: red;">99<text style="color:#fff">等级</text></text>
			</view>
			<view class="HyFlexS" style="margin: 30upx 0">
				<text style="margin-right: 10upx;">保障</text>
				<view class="HyFlexS" >
					<image style="width: 36upx;height: 36upx;" src="../../../static/img/tabbar/news.png" mode=""></image>
					实名认证</view>
				<view class="HyFlexS"  style="margin:0 30upx ">
					<image style="width: 36upx;height: 36upx;" src="../../../static/img/tabbar/news.png" mode=""></image>
					职业认证</view>
				<view class="HyFlexS"  style="margin:0 30upx ">
					<image style="width: 36upx;height: 36upx;" src="../../../static/img/tabbar/news.png" mode=""></image>
					公司认证</view>
			</view>
		</view>
		<view class="">
			<view class="">
				<view class="content">
					<view class="nuter">
						<view :class="target==0?'active':''" @click="setIndex" data-index="0">
								答复名片
						 </view>
						<view :class="target==1?'active':''" @click="setIndex" data-index="1">
								动态
						 </view>
						 <view :class="target==2?'active':''" @click="setIndex" data-index="2">
						 		服务
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
	.HyFlexS{
		display: flex;
		justify-content: start;
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
	.btn{
		background-color: #393942;
		border-radius: 20upx;
		padding: 2upx 20upx;
	}
	.nuter{
			width: 100%;
			height: 80rpx;
			line-height: 80rpx;
			display: flex;
			justify-content: space-around;
			margin-bottom: 20upx;
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
</style>