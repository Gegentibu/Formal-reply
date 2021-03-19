<template>
	<view class="activity">
		<view class="activityBox" v-for="(item,index) in dataList" :key="index" @click="gotoDt">
			<view class="activityBoxBj">
				
			</view>
			<view class="activityBoxCt">
				<view class="activityBoxCtTl">神秘大洋山环岛徒步活动3</view>
				<view class="activityBoxCtFbx">
					<view class="activityBoxCtFbxTl">
						两夜天
					</view>
					<view class="HyFlexB">
						<image class="drImg" src="../static/img/tabbar/home.png" mode=""></image>
						<text class="activityBoxCtFbxTl">活动</text>
					</view>
				</view>
				<view class="intro HyFlexB">
					<view class="introLeft">
						<text class="introLeftText">活动时间：2020.12.1 17:00至2020.12.2  16:00</text>
						<text class="introLeftText">活动地点：呼和浩特市新城区绿地智海大厦北部停车场大广场</text>
						<text class="introLeftText">每人费用：55元/每人</text>
						<text class="introLeftText">适宜人群：7-55岁之间健康人士</text>
					</view>
					<view class="introRight">
						<image class="anImg" src="../static/img/tabbar/home.png" mode=""></image>
						<text>91</text>
						<image class="anImg" src="../static/img/tabbar/home.png" mode=""></image>
						<text>91</text>
						<image class="anImg" src="../static/img/tabbar/home.png" mode=""></image>
						<text>91</text>
						<image class="anImg" src="../static/img/tabbar/home.png" mode=""></image>
					</view>
				</view>
				<view class="" style="padding:20upx 3% 0 3%; text-align: left;font-size: 22px;font-weight: 600;">
					活动费用  ¥150
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default{
		data(){
			return{
				imgUrl:this.$imgUrl
			}
		},
		// props:["content","type"],
		props:{
			dataList:{
				type:Array
			},
		},
		methods:{
			gotoDt(){
				uni.navigateTo({
					url: '/component/details',
				});
			}
		}
	}
</script>

<style>
	.activityBox{
		margin-top: 40upx;
	}
.activityBoxBj{
	width: 100%;
	height: 710upx;
	background-image: url(../static/logo.png);
	border-top-right-radius: 20upx;
	border-top-left-radius: 20upx;
}
.activityBoxCt{
	width: 100%;
	min-height: 710upx;
	border-bottom-right-radius: 20upx;
	border-bottom-left-radius: 20upx;
	background-color:#120DB5;
}
.activityBoxCtTl{
	width: 94%;
	font-size: 26px;
	height: 100upx;
	line-height: 100upx;
	font-weight: 600;
	position: relative;
	top: -100upx;
	text-align: left;
	padding: 0 3%;
	background-color: rgba(8, 9, 4, 0.5);
}
.activityBoxCtFbx{
	width: 94%;
	height: 100upx;
	line-height: 100upx;
	display: flex;
	justify-content:space-between ;
	align-items: center;
	text-align: left;
	padding: 0 3%;
	position: relative;
	top: -100upx;
	background-color: rgba(8, 9, 4, 0.5);
}
.activityBoxCtFbxTl{
	font-size: 24px;
	font-weight: 600;
}
.HyFlexB{
	display: flex;
	justify-content: space-between;
	align-items: center;
}
.drImg{
	width: 48upx;
	height: 48upx;
	margin-right: 10upx;
}
.anImg{
	width: 48upx;
	height: 48upx;
}
.intro{
	width: 94%;
	padding: 0 3%;
}
.introLeft{
	width: 90%;
}
.introRight{
	width: 10%;
	text-align: center;
}
.introLeftText{
	width: 100%;
	display: block;
	text-align: left;
	font-size: 16px;
	margin: 4upx 0;
	font-weight: 600;
}
</style>
