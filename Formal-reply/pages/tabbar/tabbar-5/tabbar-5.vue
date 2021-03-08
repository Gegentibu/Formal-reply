<template>
	<view class="Hybody">
		<view class="">
				<view class="title">
					<view class="guanggaoci">
						     上官希尔刚邀请了2位好友获得274元
					</view>
					<view class="name">
						上官喜儿
					</view>
					<view class="nameid">
						欢迎入住答复线上CBD中心
					</view>
					<view class="nameid">
						个人ID：997K4T
					</view>
					<view class="HyFlexB" style="padding:50upx 60upx 0 60upx;font-weight: 600;">
						<view class="HyFlexL">
								<image src="../../../static/img/tabbar/homeactive.png" mode=""></image>
							<view class="">
								黑钻会员
							</view>	
						</view>	
						<view class="HyFlexR">
								<image src="../../../static/img/tabbar/homeactive.png" mode=""></image>
							<view class="">
								我的主页
							</view>
						</view>	
					</view>			
				</view>
				<view class="myImg">
					<view class="myImgbox">
						<image src="../../../static/tu.jpg" mode=""></image>
					</view>
				</view>
				<view class="HyFlexB" style="padding:50upx 80upx 0 80upx;font-weight: 600;">
					<view class="HyFlexL">
						<view class="">
						</view>	
						<view class="">
							推广海报
						</view>	
					</view>	
					<view class="HyFlexR">
						<view class="">
						</view>	
						<view class="">
							我要赚钱
						</view>
					</view>	
				</view>	
				<view class="HyFlexM miaoshu">
					<view class="">
						越自律，越自由
					</view>
					<image src="../../../static/img/tabbar/me.png" mode=""></image>
				</view>
		</view>
		<view class="" style="padding:60upx 16upx 60upx 16upx;">
			<view class="menuBox">
				<view class="menuTitle HyFlexB">
					<view class="menuTitleL">
						开通会员29.99起，低至0.13元/天
					</view>
					<view class="menuTitleR">
						立即开通
					</view>
				</view>
				<view class="menuContent">
					<view class="menuList HyFlexM">
						<text>2</text>
						<image src="../../../static/img/video.png" mode=""></image>
						<view class="menuListText">
							我的收藏
						</view>
					</view>
					<view class="menuList HyFlexM">
						<text>2</text>
						<image src="../../../static/img/video.png" mode=""></image>
						<view class="menuListText">
							我的收藏
						</view>
					</view>
					<view class="menuList HyFlexM">
						<text>2</text>
						<image src="../../../static/img/video.png" mode=""></image>
						<view class="menuListText">
							我的收藏
						</view>
					</view>
					<view class="menuList HyFlexM">
						<text>2</text>
						<image src="../../../static/img/video.png" mode=""></image>
						<view class="menuListText">
							我的收藏
						</view>
					</view>
					<view class="menuList HyFlexM">
						<text>2</text>
						<image src="../../../static/img/video.png" mode=""></image>
						<view class="menuListText">
							我的收藏
						</view>
					</view>
					<view class="menuList HyFlexM">
						<text>2</text>
						<image src="../../../static/img/video.png" mode=""></image>
						<view class="menuListText">
							我的收藏
						</view>
					</view>
				</view>
			</view>
			<view class="">
				<view class="HyFlexB">
					<view class="fontS">
						我的答复CBD中心
					</view>
					<view class="fontS">
						>
					</view>
				</view>
				<view class="fontS2">
					财务中心
				</view>
				<view style="padding: 0upx 32upx;">
					<view class="tx">
						<view class="tixian HyFlexB" v-for="(item,index) in Tixiandata" :key="index">
							<view class="tixianL">
								<view class="tixianLt">
									服务收入
								</view>
								<view class="tixianLn">
									￥0.00
								</view>
							</view>
							<view class="tixianR">
								提现
							</view>
						</view>
					</view>
				</view>
			</view>
			<view class="">
				<view class="HyFlexB">
					<view class="fontS">
							尊享VIP会员中心
					</view>
					<view class="fontS">
						>
					</view>
				</view>
			</view>
		</view>
		
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: 'Hello',
				Tixiandata:[{},{},{},{},{}]
			}
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style>
	.Hybody {
		/* padding: 0 32upx; */
		height: 2200upx;
		font-size: 12px;
		background-color: #080808;
		color: #fff;
	}
	.title{
		text-align: center;
		height: 360upx;
		background-color: rgba(18, 13, 181, 100);
		border-bottom-left-radius: 40px;
		border-bottom-right-radius: 40px;
	}
	
	.guanggaoci{
		height: 50upx;
		font-size: 16px;
		line-height: 50upx;
	}
	.name{
		font-family: 方正工业黑-标准;
		font-weight: 600;
		font-size: 26px;
		margin: 20upx 0;
	}
	.nameid{
		margin: 10upx 0;
		font-size: 14px;
		color: rgb(153, 155, 178);
	}
	.HyFlexB{
		display: flex;
		justify-content: space-between;
		align-items: center;
		font-size: 14px;
	}
	.HyFlexB image{
		width: 34upx;
		height: 34upx;
	}
	.HyFlexM{
		display: flex;
		justify-content: center;
		align-items: center;
	}
	.HyFlexL{
		display: flex;
		justify-content: flex-start;
		align-items: center;
	}
	.HyFlexR{
		display: flex;
		justify-content: flex-end;
		align-items: center;
	}
	.myImg{
		display: flex;
		justify-content: center;
		position: relative;
	}
	.myImgbox{
		width: 200upx;
		height: 200upx;
		display: flex;
		justify-content: center;
		border-radius: 50%;
		border: 8px solid #080808;
		position: absolute;
		top: -104upx;
	}
	.myImg image{
		width: 200upx;
		height: 200upx;
		border-radius: 50%;
	}
	.miaoshu {
		margin-top: 50upx;
	}
	.miaoshu image{
		width: 24upx;
		height: 24upx;
	}
	.menuBox{
		padding-bottom: 60upx;
		border-bottom: 1px solid #3B3838 ;
	}
	.menuContent{
		display: flex;
		justify-content: center;
		align-items: center;
		flex-wrap: wrap;
	}
	.menuTitle{
		height: 90upx;
		color: #fff;
	}
	.menuTitleL{
		width: 75%;
		height: 90upx;
		line-height: 90upx;
		background-color: #393942;
		text-align: center;
		border-top-left-radius: 40px;
	}
	.menuTitleR{
		width: 25%;
		height: 90upx;
		line-height: 90upx;
		background-color: #EE0707;
		text-align: center;
		border-top-right-radius: 40px;
	}
	.menuList {
		width: 200upx;
		height: 200upx;
		margin: 0 20upx;
		flex-wrap: wrap;
	}
	.menuList text{
		width: 100upx;
		margin: 0 50upx;
		text-align: end;
		position: relative;
		top: 30upx;
		color: #EE0707;
		font-size: 14px;
		font-weight: 600;
	}
	.menuListText {
		width: 200upx;
		text-align: center;
	}
	.menuList image{
		width: 60upx;
		height: 60upx;
	}
	.fontS{
		color: rgba(255, 255, 255, 100);
		font-size: 22px;
		text-align: left;
		font-weight: 600;
		font-family: 方正工业黑-标准;
		padding: 20upx 32upx;
	}
	.fontS2{
		font-size: 18px;
		color: rgba(255, 255, 255, 100);
		text-align: left;
		font-weight: 600;
		font-family: 方正工业黑-标准;
		margin-bottom: 10upx;
		padding: 10upx 32upx;
	}
	.tixian{
		padding: 22upx 0;
		font-size: 16px;
		border-bottom: 1px solid #787B7B;
	}
	.tixianLt{
		width: 100%;
	}
	.tixianLn{
		width: 100%;
	}
	.tixianR{
		padding: 10upx 45upx;
		border-radius: 10upx;
		background-color: #787B7B;
		color: #080808;
	}
	.tx .tixian:nth-last-child(1){
		border-bottom: none;
	}
	.tx{
		padding: 10upx 32upx;
		background-color: #171616;
		border-radius: 15upx;
	}
</style>
