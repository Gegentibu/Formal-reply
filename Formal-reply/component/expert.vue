<template>
	<view class="expert">
		<view class="expertBox" v-for="(item,index) in dataList" :key="index">
			<view class="expertBoxBj">
				
			</view>
			<view class="expertBoxCt">
				<view class="expertBoxCtTl">与达人交朋友拓展新的人脉</view>
				<view class="expertBoxCtFbx">
					<view class="expertBoxCtFbxTl">
						个人名片卡
					</view>
					<view class="HyFlexB">
						<image class="drImg" src="../static/img/tabbar/home.png" mode=""></image>
						<text class="expertBoxCtFbxTl">达人</text>
					</view>
				</view>
				<view class="intro HyFlexB">
					<view class="introLeft">
						<text class="introLeftText">个人简迅：女   37岁</text>
						<text class="introLeftText">达人职业：教育行业  英语老师</text>
						<text class="introLeftText">所在地区：内蒙古.呼和浩特</text>
						<text class="introLeftText">达人职务：创始人兼CEO</text>
						<text class="introLeftText">单位信息：内蒙古餐企云网络科技有限公司</text>
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
					刘涛
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

		}
	}
</script>

<style>
	.expertBox{
		margin-bottom: 40upx;
	}
.expertBoxBj{
	width: 100%;
	height: 710upx;
	background-image: url(../static/tu.jpg);
	border-top-right-radius: 20upx;
	border-top-left-radius: 20upx;
}
.expertBoxCt{
	width: 100%;
	min-height: 710upx;
	border-bottom-right-radius: 20upx;
	border-bottom-left-radius: 20upx;
	background-color:#120DB5;
}
.expertBoxCtTl{
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
.expertBoxCtFbx{
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
.expertBoxCtFbxTl{
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
