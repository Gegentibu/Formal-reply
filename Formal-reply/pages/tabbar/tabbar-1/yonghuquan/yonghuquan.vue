<template>
	<view class="Hybody">
		<view class="comment" v-show="isComment">
			<view class="HyFlexB" style="padding: 0 20upx;">
				<view class="">
					
				</view>
				<view class="">
					321条评论
				</view>
				<view class="" style="font-size: 20px;" @click="closeComment">
					×
				</view>
			</view>
			<view class="HyFlexB" style="padding:10px;">
				<view >
					<image class="commentPimg" src="../../../../static/tu.jpg" mode=""></image>
				</view>
				<view class="" style="width: 500upx;">
					<view class="" style="color: #787B7B;">
						爱的故事
					</view>
					<view class="">
						这才是一个城市的综合素质
					</view>
				</view>
				<view class="">
					<view class="HyFlexM" style="line-height: 40upx;">
						24<image class="commentBimg" src="../../../../static/img/tabbar/guanzhuactive.png" mode=""></image>
					</view>
					<view class="">
						2020.09.02
					</view>
				</view>
			</view>
			<view class="HyFlexB" style="padding:10px;">
				<view >
					<image class="commentPimg" src="../../../../static/tu.jpg" mode=""></image>
				</view>
				<view class="" style="width: 500upx;">
					<view class="" style="color: #787B7B;">
						爱的故事
					</view>
					<view class="">
						这才是一个城市的综合素质
					</view>
				</view>
				<view class="">
					<view class="HyFlexM" style="line-height: 40upx;">
						24<image class="commentBimg" src="../../../../static/img/tabbar/guanzhuactive.png" mode=""></image>
					</view>
					<view class="">
						2020.09.02
					</view>
				</view>
			</view>
			<view class="commentInput">
				<input type="text" value="" />
			</view>
		</view>
		<view class="fontS">
			答复CBD用户圈动态
		</view>
		<view class="" style="margin-bottom: 30upx;">
			在这里您可以看见很多陌生用户的动态信息
		</view>
		<view class="">
			<view class="YhqList" v-for="(item,index) in 3" :key="index">
				<view class="" style="width: 12%;">
					<image class="headP" src="../../../../static/tu.jpg" mode=""></image>
				</view>
				<view class="" style="width: 86%;">
					<view class="" style="font-size: 16px;font-weight: 600;height: 80upx;line-height: 80upx;">
						美丽的晚霞
					</view>
					<view v-if="index>0" class="" style="transform:scale(1,0.82);">
						<service :dataList="dataList"></service>
					</view>
					<view v-else-if="index<1" class="">
						<view class="" style="line-height: 50upx;font-size: 14px;">
							吉林省大家疯狂的世界纪录甲方都是减肥解决 了解了解
							了计算机房龙卷风了解放军队酸辣粉
						</view>
						<view  class="YhqImgList">
							<view v-for="(i,l) in 4" :key="l">
								<image src="../../../../static/huodong.png" mode=""></image>
							</view>
						</view>
					</view>
					<view class="HyflexB" :style=" index<1?'margin-top: 10px;':'margin-top: -80rpx;'">
						<view class="" style="font-size: 16px;font-weight: 600;width: 60%; text-indent:1em;">
							活动
						</view>
						<view class="">
							<image class="YhqBtn" src="../../../../static/img/tabbar/guanzhuactive.png" mode=""></image>
							<image @click="openComment" class="YhqBtn"  src="../../../../static/img/tabbar/guanzhuactive.png" mode=""></image>
							<image class="YhqBtn"  src="../../../../static/img/tabbar/guanzhuactive.png" mode=""></image>
						</view>
					</view>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	import service from '../../../../component/service.vue'
	export default {
		components:{
				service
		},
		data() {
			return {
				dataList:[{}],
				isComment:false
				}
			},
			methods:{
				openComment(){
					this.isComment = true;
				},
				closeComment(){
					this.isComment =false;
				}
			}
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
	.HyFlexB,.HyflexB{
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
		margin-top: 20upx;
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
		width: 293upx;
		height: 293upx;
		
	}
	.comment{
		width: 750upx;
		background-color: #28272D;
		position: fixed;
		bottom: 0;
		height: 650upx;
		border-top-left-radius: 20upx;
		border-top-right-radius: 20upx;
		z-index: 9999999;
		left: 0;
	}
	.commentPimg{
		width: 60upx;
		height: 60upx;
		border-radius: 50%;
	}
	.commentBimg{
		width: 40upx;
		height: 40upx;
		border-radius: 50%;
	}
	.commentInput{
		    width: 92%;
		    height: 50rpx;
		    background: #787B7B 10000%;
		    border-radius: 30rpx;
		    line-height: 50rpx;
		    color: #fff;
		    margin-left: 4%;
		    position: fixed;
		    bottom: 10rpx;
		    z-index: 99999999;
			text-indent: 1em;
	}
</style>