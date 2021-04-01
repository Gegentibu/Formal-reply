<template>
	<view class="Hybody">
<!-- 		<view class="titleText">
			我的收藏
		</view> -->
		<view class="" style="margin: 20upx 0;">
			<view class="content">
				<view class="nuter">
					<view :class="target==0?'active':''" @click="setIndex" data-index="0">
							我的关注
					 </view>
					<view :class="target==1?'active':''" @click="setIndex" data-index="1">
							关注我的
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
						<guanzhu :dataList="dataList"></guanzhu>
						<!-- 按顺序对应第一个的内容 -->
						<!-- <rectangle id="swiperHeight" :dataList="dataList"></rectangle> -->
					</swiper-item>
					<swiper-item>
						<guanzhu :dataList="dataList"></guanzhu>
						<!-- 按顺序对应第二个的内容 -->
						<!-- <rectangle :dataList="dataList"></rectangle> -->
					</swiper-item>
				</swiper>
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
					target:0,
					swiperHeight:'height:500px',
					thisindex:0,
					dataList:[{},{},{}],
	            }
	        },
	        onLoad() {
				
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
</style>