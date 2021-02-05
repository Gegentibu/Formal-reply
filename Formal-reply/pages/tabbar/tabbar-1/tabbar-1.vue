<template>
	<view class="Hybody">
		<view class="header HyFlexB">
			<view class="headerImg HyFlexAb">
				<image src="../../../static/logo.png" mode=""></image> 
				<text>上官喜儿</text>
			</view>
			<view class="PositionImg HyFlexM">
				<image src="../../../static/logo.png" mode=""></image>
				<text>上海</text>
			</view>
		</view>
		<view class="titleF">
			答复CBD中心导航
		</view>
		<view class="formlNav HyFlexB">
			<view v-for="(item,index) in NavOptions" :key="index" class="Nav">
				<view class="NavImage">
					<view style="width: 100%;color: #F5AB36;text-indent:20upx;">●</view>
					<image src="../../../static/img/release.png" mode=""></image>
					<view style="width: 100%;text-align: center;font-size: 14px;line-height: 14px;">达人</view>
				</view>
			</view>
		</view>
		<view class="Cof">
			用户圈
		</view>
		<view class="content">
			<view class="nuter">
				<view :class="target==0?'active':''" @click="setIndex" data-index="0">
				 		热门活动
				 </view>
				<view :class="target==1?'active':''" @click="setIndex" data-index="1">
						推荐活动
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
					<!-- 按顺序对应第一个的内容 -->
					<rectangle :dataList="dataList"></rectangle>
				</swiper-item>
				<swiper-item>
					<!-- 按顺序对应第二个的内容 -->
					<rectangle :dataList="dataList"></rectangle>
				</swiper-item>
			</swiper>
		</view>
		<view class="content">
			<view class="nuter">
				<view :class="target2==0?'active':''" @click="setIndex2" data-index="0">
				 		热门达人
				 </view>
				<view :class="target2==1?'active':''" @click="setIndex2" data-index="1">
						推荐达人
				 </view>
			</view>
			<swiper 
			:duration="500" 
			:current="thisindex2"  
			:data-index='thisindex2' 
			@change="toggle2"
			:style="swiperHeight2"
			circular>
				<swiper-item>
					<!-- 按顺序对应第一个的内容 -->
					<expert :dataList="dataList"></expert>
				</swiper-item>
				<swiper-item>
					<!-- 按顺序对应第二个的内容 -->
					<expert :dataList="dataList"></expert>
				</swiper-item>
			</swiper>
		</view>		
	</view>
</template>

<script>
	import rectangle from '../../../component/rectangle.vue'
	import expert from '../../../component/expert.vue'
export default {
	components:{
			rectangle,
			expert
	},
	data() {
		return {
			NavOptions:[{},{},{},{},{},{}],
			target:0,
			// 当前item位置
			thisindex:0,
			swiperHeight:0,
			target2:0,
			// 当前item位置
			thisindex2:0,
			swiperHeight2:0,
			dataList:[{},{},{}]
			}
		},
		methods: {
			// 切换触发的事件
			toggle(e){
					let index = e.detail.current
					this.target = index
				},			
			// 切换触发的事件
			toggle2(e){
					let index = e.detail.current
					this.target2 = index
				},
			// 点击nav控制下面的展示
			setIndex(e){
			let index = e.currentTarget.dataset.index
			this.thisindex = index
			},
			// 点击nav控制下面的展示
			setIndex2(e){
			let index = e.currentTarget.dataset.index
			this.thisindex2 = index
			},			
		},
		onLoad() {
			this.swiperHeight ='height:'+this.dataList.length*169+'px'
			this.swiperHeight2 ='height:'+this.dataList.length*169+'px'
		}
};
</script>

<style>
	.nuter{
		width: 100%;
		height: 80rpx;
		line-height: 80rpx;
		display: flex;
		justify-content: flex-start;
	}
	.nuter view{
		/* flex: 1; */
		/* font-size: 30rpx; */
		text-align: center;
		transition: all 0.5s ease .1s;
		/* background-color: #f0f0f0; */
		text-align: left;
		margin-right: 20upx;
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
		font-size: 18px;
		font-family: '方正工业黑-标准';
		font-weight: 600;
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
.Hybody {
	padding: 32upx;
	margin-top: 26upx;
	font-size: 12px;
	background-color: #080808;
	color: #fff;
}
.headerImg text{
	font-size: 14px;
	color: #787B7B;
}
.headerImg image{
	width: 90upx;
	height: 90upx;
	border-radius: 70upx;
}
.PositionImg text{
	color: #fff;
	font-weight: 600;
}
.PositionImg image{
	width: 48upx;
	height: 48upx;
}
.HyFlexM{
	display: flex;
	justify-content: center;
	align-items: center;
}
.HyFlexB{
	display: flex;
	justify-content: space-between;
	align-items: center;
}
.HyFlexAb{
	display: flex;
	justify-content: center;
	align-items: flex-end;
}
.titleF{
	font-size: 18px;
	font-family: '方正工业黑-标准';
	margin-top: 46upx;
	margin-bottom: 6upx;
	font-weight: 600;
}
.formlNav{
	flex-wrap: wrap;
}
.Nav{
	margin-top: 40upx;
}
.NavImage{
	width: 208upx;
	height: 278upx;
	border-radius: 16px;
	background-color: #23273D;
	display: flex;
	flex-wrap: wrap ;
	align-items: center;
	justify-content: center;
}
.NavImage image{
	/* margin: 62upx 50upx; */
	width: 108upx;
	height: 154upx;
}
.Cof{
	width: 100%;
	height: 194upx;
	font-size: 18px;
	font-family: '方正工业黑-标准';
	margin-top: 46upx;
	margin-bottom: 46upx;
	text-align: center;
	line-height: 242upx;
	font-weight: 600;
	background-image: url(../../../static/img/cof.png);
	background-repeat: 100%;
}
</style>
