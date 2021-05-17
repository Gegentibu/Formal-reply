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
						<view class="HyFlexL" @click="goToUrl('黑钻会员')">
								<image src="../../../static/img/tabbar/homeactive.png" mode=""></image>
							<view class="">
								黑钻会员
							</view>	
						</view>	
						<view class="HyFlexR"  @click="goToUrl('我的主页')">
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
					<view class="HyFlexL"  @click="goToUrl('推广海报')">
						<view class="">
						</view>	
						<view class="">
							推广海报
						</view>	
					</view>	
					<view class="HyFlexR"  @click="goToUrl('我要赚钱')">
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
		<view class="" style="padding:60upx 16upx 10upx 16upx;">
			<view class="menuBox">
				<view class="menuTitle HyFlexB">
					<view class="menuTitleL">
						开通会员29.99起，低至0.13元/天
					</view>
					<view class="menuTitleR"  @click="goToUrl('立即开通')">
						立即开通
					</view>
				</view>
				<view class="menuContent">
					<view class="menuList HyFlexM"  @click="goToUrl('我的收藏')">
						<text>2</text>
						<image src="../../../static/img/video.png" mode=""></image>
						<view class="menuListText">
							我的收藏
						</view>
					</view>
					<view class="menuList HyFlexM"  @click="goToUrl('我的关注')">
						<text>2</text>
						<image src="../../../static/img/video.png" mode=""></image>
						<view class="menuListText">
							我的关注
						</view>
					</view>
					<view class="menuList HyFlexM"  @click="goToUrl('我的订单')">
						<text>2</text>
						<image src="../../../static/img/video.png" mode=""></image>
						<view class="menuListText">
							我的订单
						</view>
					</view>
					<view class="menuList HyFlexM"  @click="goToUrl('主页设置')">
						<text>2</text>
						<image src="../../../static/img/video.png" mode=""></image>
						<view class="menuListText">
							主页设置
						</view>
					</view>
					<view class="menuList HyFlexM"  @click="goToUrl('认证管理')">
						<text>2</text>
						<image src="../../../static/img/video.png" mode=""></image>
						<view class="menuListText">
							认证管理
						</view>
					</view>
					<view class="menuList HyFlexM" @click="goToUrl('我的审核')">
						<text>2</text>
						<image src="../../../static/img/video.png" mode=""></image>
						<view class="menuListText">
							我的审核
						</view>
					</view>
				</view>
			</view>
			<view class="">
				<view class="HyFlexB" style="padding: 0upx 32upx;">
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
							<view class="tixianR"  @click="goToUrl('提现')">
								提现
							</view>
						</view>
					</view>
				</view>
			</view>
			<view class="" style="padding: 0upx 32upx;">
				<view class="">
					<view class="HyFlexB">
						<view class="fontS">
								尊享VIP会员中心
						</view>
						<view class="fontS">
							>
						</view>
					</view>
					<view class="HyFlexM Hykp">
						<view class="HyFlexB wdt100">
							<view class="" style="font-size: 20px;font-weight: 400;">
								答复.尊享VIP
							</view>
							<view class="" style="font-size: 16px;">
								最低￥29.99/月
							</view>
						</view>
						<view class="HyFlexB wdt100">
							<view class="HyFlexM" style="flex-wrap: wrap;width: 65%;justify-content: start;">
								<view class="" >
									推荐开通<text style="color: #4CD964;">铂金</text>以上会员
								</view>
								<view class="" style="margin: 10upx 0;">
									推广最高每一笔奖励<text style="color: #4CD964;">275</text>元
								</view>
							</view>
							<view class="Hybtn"  @click="goToUrl('会员中心')">
								会员中心
							</view>
						</view>
					</view>
				</view>
			</view>
			<view class="" style="padding: 0upx 32upx;">
				<view class="">
					<view class="HyFlexB">
						<view class="fontS">
								答复黑卡中心
						</view>
						<view class="fontS">
							>
						</view>
					</view>
					<view class="HyFlexM Hykp">
						<view class="HyFlexB wdt100">
							<view class="" style="font-size: 20px;font-weight: 400;">
								答复黑卡                
							</view>
							<view class="Hybtn"  @click="goToUrl('开通黑卡')">
								开通黑卡
							</view>
						</view>
						<view class="HyFlexB wdt100">
							<view class="HyFlexM" style="flex-wrap: wrap;width: 100%;justify-content: start;">
								<view class="" >
									是您尊贵身份的象征
								</view>
								<view class="" style="margin: 10upx 0;">
									开通后超低价格购买已入住黑卡实体商家线下服务
								</view>
							</view>
						</view>
					</view>
				</view>
			</view>
		</view>
		<view class="" style="padding: 10upx 32upx;">
			<view class="fontS" style="text-align: center;">
				为您推荐
			</view>
			<view class="fontS">
				活动
			</view>
			<view class="HyFlexB" style="justify-content: space-around;">
				<image class="Wdhuodong" src="../../../static/tu.jpg" mode=""></image>
				
				<image class="Wdhuodong" src="../../../static/tu.jpg" mode=""></image>
			</view>
			<view class="fontS">
				达人
			</view>
			<view class="HyFlexB" style="justify-content: space-around;">
				<view class="HyFlexB" style="width: 200upx;flex-wrap: wrap;justify-content: center;">
					<image class="Wddaren" src="../../../static/tu.jpg" mode=""></image>
					<text style="margin: 10upx 0;">郊野公园慢跑</text>
				</view>
				<view class="HyFlexB" style="width: 200upx;flex-wrap: wrap;justify-content: center;">
					<image class="Wddaren" src="../../../static/tu.jpg" mode=""></image>
					<text style="margin: 10upx 0;">郊野公园慢跑</text>
				</view>
			</view>
			<view class="fontS">
				服务
			</view>
			<view class="release">	
				<view class="releaseBj">
					<text class="releaseBjTitle">让好产品走出去让更多人购买</text>
					<text class="releaseBjText">在这里您可以出售您公司或代理产品及朋友的产品来互动营销，让指尖生意源源不断的继续。</text>
				</view>
			</view>
			<view class="fontS">
				三方服务
			</view>
			<view class="HyFlexB">
				<view class="HyFlexB" style="width: 200upx;flex-wrap: wrap;justify-content: center;">
					<image class="Wdsanfang" src="../../../static/tu.jpg" mode=""></image>
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
			goToUrl(e){
				if(e=='黑钻会员'){
					uni.navigateTo({
						url: '/pages/tabbar/tabbar-9/tabbar-9',
					});
				}
				if(e=='立即开通'){
					uni.navigateTo({
						url: '/pages/tabbar/tabbar-9/tabbar-9',
					});
				}
				if(e=='我要赚钱'){
					uni.navigateTo({
						url: '/pages/tabbar/tabbar-9/tabbar-9',
					});
				}
				if(e=='会员中心'){
					uni.navigateTo({
						url: '/pages/tabbar/tabbar-9/tabbar-9',
					});
				}
				if(e=='我的主页'){
					uni.navigateTo({
						url: '/pages/tabbar/tabbar-7/tabbar-7',
					});
				}
				if(e=='推广海报'){
					uni.navigateTo({
						url: '/pages/tabbar/tabbar-6/tuiguanghaibao',
					});
				}
				if(e=='我的收藏'){
					uni.navigateTo({
						url: '/pages/tabbar/tabbar-6/wodeshoucang',
					});
				}
				if(e=='我的关注'){
					uni.navigateTo({
						url: '/pages/tabbar/tabbar-6/wodeguanzhu',
					});
				}
				if(e=='我的订单'){
					uni.navigateTo({
						url: '/pages/tabbar/tabbar-6/wodedingdan',
					});
				}
				if(e=='主页设置'){
					uni.navigateTo({
						url: '/pages/tabbar/tabbar-6/zhuyeshezhi',
					});
				}
				if(e=='认证管理'){
					uni.navigateTo({
						url: '/pages/tabbar/tabbar-6/renzhengguanli',
					});
				}
				if(e=='我的审核'){
					uni.navigateTo({
						url: '/pages/tabbar/tabbar-6/shenhefankui',
					});
				}
				if(e=='提现'){
					uni.navigateTo({
						url: '/pages/tabbar/tabbar-8/tixian',
					});
				}
				if(e=='开通黑卡'){
					uni.navigateTo({
						url: '/pages/tabbar/tabbar-10/tabbar-10',
					});
				}
				
			}
		}
	}
</script>

<style>
	.Hybody {
		/* padding: 0 32upx; */
		height: 5000upx;
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
		margin: 0 18upx;
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
		padding: 20upx 0upx;
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
	.Hykp{
		padding: 10upx;
		border-radius: 15upx;
		background-color: #2C2D28;
		flex-wrap: wrap;
	}
	.wdt100{
		width: 94%;
		padding: 3%;
	}
	.Hybtn{
		display: block;
		padding:10upx 30upx;
		border-radius: 30upx;
		background-color: rgba(18, 13, 181, 100);
		color: rgba(254, 255, 249, 100);
		font-size: 14px;
		text-align: center;
		font-family: Microsoft Yahei;
	}
	.HyFlexB .Wdhuodong{
		width: 260upx;
		height: 260upx;
		border-radius: 10upx;
	}
	.HyFlexB .Wddaren{
		width: 104upx;
		height: 104upx;
		border-radius: 50%;
	}
	.HyFlexB .Wdsanfang{
		width: 154upx;
		height: 154upx;
		border-radius: 50%;
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
</style>
