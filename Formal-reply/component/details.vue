<template>
	<view class="details">
		<view class="detailsBox">
			<view class="detailsBoxBj">
				
			</view>
			<view class="detailsBoxCt">
				<view class="detailsBoxCtTl">神秘大洋山环岛徒步活动3</view>
				<view class="detailsBoxCtFbx">
					<view class="detailsBoxCtFbxTl">
						两夜天
					</view>
					<view class="HyFlexB">
						<image class="drImg" src="../static/img/tabbar/home.png" mode=""></image>
						<text class="detailsBoxCtFbxTl">支持退款</text>
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
				<view class="HyFlexM">
					<view class="gmBtn HyFlexAr">
						<view class="">
							
						</view>
						<view class="">
							点击购买
						</view>
						<view class="HyFlexM">
							<image src="../static/img/tabbar/newsactive.png" mode="" style="width: 40upx;height: 40upx;"></image>
						</view>
					</view>
				</view>
				<view class="cpXq">
					产品详情
				</view>
				<view class="ggImg">
					<image src="../static/tu.jpg" mode=""></image>
					<image src="../static/tu.jpg" mode=""></image>
					<image src="../static/tu.jpg" mode=""></image>
					<image src="../static/tu.jpg" mode=""></image>
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
	.detailsBox{
		margin-top: 40upx;
	}
.detailsBoxBj{
	width: 100%;
	height: 710upx;
	background-image: url(../static/logo.png);
	border-top-right-radius: 20upx;
	border-top-left-radius: 20upx;
}
.detailsBoxCt{
	width: 100%;
	min-height: 710upx;
	border-bottom-right-radius: 20upx;
	border-bottom-left-radius: 20upx;
	background-color:#120DB5;
}
.detailsBoxCtTl{
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
.detailsBoxCtFbx{
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
.detailsBoxCtFbxTl{
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
.HyFlexB{
	display:flex;
	justify-content: space-between;
	align-items: center;
}
.HyFlexAr{
	display:flex;
	justify-content: space-around;
	align-items: center;
}
.HyFlexM{
	display: flex;
	justify-content: center;
	align-items: center;
}
.gmBtn{
	width: 360rpx;
	border-radius: 57upx;
	background-color: rgba(18, 13, 181, 100);
	text-align: center;
	box-shadow: 0px 2px 6px 0px rgba(0, 0, 0, 0.4);
	border: 1px solid rgba(255, 255, 255, 100);
	margin: 30upx 0;
	line-height: 2.5;
}
.cpXq{
	font-family: 方正汉真广标-标准;
	text-align: center;
	font-size: 24px;
	font-weight: 600;
	margin: 40upx 0;
}
.ggImg image{
	width: 750upx;
}
</style>
