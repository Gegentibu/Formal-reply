<template>
	<view class="service">
		<view class="serviceBox" v-for="(item,index) in dataList" :key="index">
			<view class="serviceBoxBj">
				
			</view>
			<view class="serviceBoxCt">
				<view class="serviceBoxCtTl">内蒙古锡林郭勒草原羊全羊礼盒</view>
				<view class="introBox">
					<view class="introText">
						<image src="../static/img/tabbar/guanzhu.png" mode=""></image>
						<text>2020/10/02 （显示产品发布时间）</text>
					</view>
					<view class="introText">
						<image src="../static/img/tabbar/guanzhu.png" mode=""></image>
						<text>杨树浦路 6.5KM外</text>
					</view>
					<view class="introText">
						<image src="../static/img/tabbar/guanzhu.png" mode=""></image>
						<text>1680元/人 </text>
					</view>
				</view>
				<view class="introFo HyFlexL">
					<view class="HyFlexL">
						<image class="anImg" src="../static/img/tabbar/home.png" mode=""></image>
						<text>91</text>
					</view>
					<view class="HyFlexL">
						<image class="anImg" src="../static/img/tabbar/home.png" mode=""></image>
						<text>91</text>
					</view>
					<view class="HyFlexL">
						<image class="anImg" src="../static/img/tabbar/home.png" mode=""></image>
						<text>91</text>
					</view>
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
	.service{
		width: 100%;
	}
	.serviceBox{
		margin-bottom: 40upx;
		overflow: hidden;
		height: 710upx;
	}
.serviceBoxBj{
	width: 100%;
	height: 710upx;
	background-image: url(../static/tu.jpg);
	border-top-right-radius: 20upx;
	border-top-left-radius: 20upx;
	border-bottom-right-radius: 20upx;
	border-bottom-left-radius: 20upx;
}
.serviceBoxCt{
	width: 100%;
	min-height: 360upx;
	border-bottom-right-radius: 20upx;
	border-bottom-left-radius: 20upx;
}
.serviceBoxCtTl{
	width: 94%;
	font-size: 22px;
	height: 100upx;
	line-height: 100upx;
	font-weight: 600;
	position: relative;
	top: -400upx;
	text-align: left;
	padding: 0 3%;
	background-color: rgba(8, 9, 4, 0.5);
}
.serviceBoxCtFbx{
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
.serviceBoxCtFbxTl{
	font-size: 24px;
	font-weight: 600;
}
.HyFlexB{
	display: flex;
	justify-content: space-between;
	align-items: center;
}
.HyFlexC{
	display: flex;
	justify-content: center;
	align-items: center;
}
.HyFlexL{
	display: flex;
	justify-content: left;
	align-items: center;
}
.introText image{
	width: 48upx;
	height: 48upx;
	margin-right: 10upx;
}
.anImg{
	width: 48upx;
	height: 48upx;
	margin-right: 30upx;
}
.introBox{
	width: 94%;
	font-size: 14px;
	height: 300upx;
	line-height: 100upx;
	font-weight: 600;
	position: relative;
	top: -400upx;
	text-align: left;
	padding: 0 3%;
	background-color: rgba(8, 9, 4, 0.5);
}
.introText{
	height: 60upx;
	display: flex;
	align-items: center;
}
.introFo{
	width: 94%;
	font-size: 15px;
	height: 100upx;
	line-height: 100upx;
	font-weight: 600;
	position: relative;
	top: -500upx;
	text-align: left;
	padding: 0 3%;
}
.HyFlexL text{
	margin-right: 20upx;
}
</style>
