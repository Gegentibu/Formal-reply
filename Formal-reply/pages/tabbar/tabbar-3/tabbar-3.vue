<template>
	<view class="Hybody">
		<view class="fontS">
			答复CBD用户圈动态
		</view>
		<view class="" style="margin-bottom: 30upx;">
			在这里您可以看见很多陌生用户的动态信息
		</view>
		<view class="">
			<view class="YhqList" v-for="(item,index) in 3" :key="index">
				<view class="" style="width: 12%;">
					<image class="headP" src="../../../static/img/qa.png" mode=""></image>
				</view>
				<view class="" style="width: 86%;">
					<view class="" style="font-size: 16px;font-weight: 600;height: 80upx;line-height: 80upx;">
						美丽的晚霞
					</view>
					<view class="" style="transform:scale(1,0.82);">
						<service :dataList="dataList"></service>
					</view>
<!-- 					<view class="" style="line-height: 50upx;font-size: 14px;">
						吉林省大家疯狂的世界纪录甲方都是减肥解决 了解了解
						了计算机房龙卷风了解放军队酸辣粉
					</view>
					<view  class="YhqImgList">
						<view v-for="(i,l) in 4" :key="l">
							<image src="../../../static/img/video.png" mode=""></image>
						</view>
					</view> -->
					<view class="HyflexB">
						<view class="" style="font-size: 16px;font-weight: 600;width: 60%; text-indent:1em;">
							活动
						</view>
						<view class="">
							<image class="YhqBtn" src="../../../static/img/tabbar/guanzhuactive.png" mode=""></image>
							<image class="YhqBtn"  src="../../../static/img/tabbar/guanzhuactive.png" mode=""></image>
							<image class="YhqBtn"  src="../../../static/img/tabbar/guanzhuactive.png" mode=""></image>
						</view>
					</view>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	import service from '../../../component/service.vue'
	export default {
		components:{
				service
		},
		data() {
			return {
				dataList:[{}]
				}
			},
		}
</script>

<style>
	.Hybody{
		padding: 0 32upx;
		height: 100%;
		font-size: 12px;
		background-color: #080808;
		color: #fff;
		font-family: 方正工业黑-标准;
	}
	.HyFlexM{
		display: flex;
		justify-content: center;
		align-items: center;
	}
	.HyflexB{
		display: flex;
		justify-content: space-between;
		align-items: center;
	}
	.fontS{
		font-size: 18px;
		color: rgba(255, 255, 255, 100);
		text-align: left;
		font-weight: 600;
		margin-bottom: 10upx;
		padding: 10upx 0;
	}
	.YhqList{
		display: flex;
		justify-content: space-between;
		align-items: flex-start;
		margin: 20upx 0;
	}
	.headP{
		width: 80upx;
		height: 80upx;
		border-radius: 50%;
	}
	.YhqBtn{
		width: 44upx;
		height: 44upx;
		margin: 0 10upx;
	}
	.YhqImgList{
		display: flex;
		justify-content: space-between;
		align-items: center;
		flex-wrap: wrap;
	}
	.YhqImgList image{
		width: 290upx;
		height: 290upx;
		
	}
</style>