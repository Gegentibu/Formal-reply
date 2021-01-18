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
		<view class="formlNav">
			<view v-for="(item,index) in NavOptions" :key="index" class="Nav">
				
			</view>
		</view>
	</view>
</template>

<script>
export default {
	data() {
		return {
			NavOptions:[{},{},{},{},{},{}]
		};
	},
	onLoad() {},
	methods: {}
};
</script>

<style>
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
	margin: 46upx 0;
}
</style>
