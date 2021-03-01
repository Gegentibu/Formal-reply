<template>
	<view class="rectangle">
		<view class="rectangleBox" v-for="(item,index) in dataList" :key="index">
			<view class="rectangleLeft">
				<image src="../static/tu.jpg" mode=""></image>
			</view>
			<view class="rectangleRight">
				<view class="text" style="font-size: 18px;font-weight: 600;">
					神秘大洋山环岛徒步</view>
				<view class="text">
					<image src="../static/img/tabbar/home.png" mode=""></image>
					2020/09/25 7:00-17:00</view>
				<view class="text">
					<image src="../static/img/tabbar/home.png" mode=""></image>
					大洋山环岛 10.5KM外</view>
				<view class="text">
					<image src="../static/img/tabbar/home.png" mode=""></image>
					55元/人</view>
				<view class="rectangleRightFooter">
					<view class="rectangleRightBig">
						<image src="../static/img/tabbar/home.png" mode=""></image>
						42
					</view>
					<view class="rectangleRightBig">
						<image src="../static/img/tabbar/home.png" mode=""></image>
						105
					</view>
					<view class="rectangleRightBig">
						<image src="../static/img/tabbar/home.png" mode=""></image>
						91
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
	.rectangleBox{
		width: 100%;
		display: flex;
		justify-content: center;
		align-items: center;
		flex-wrap: no-wrap;
		border-radius: 38upx;
		margin-bottom: 30upx;
	}
	.rectangleLeft {
		width: 260upx;
		margin: 24upx;
		display: flex;
		justify-content: space-between;
	}
	.rectangleLeft image{
		width: 260upx;
		height: 260upx;
		border-radius: 40upx;
	}
	.rectangleRight{
		width: 340upx;
		display: flex;
		justify-content: start;
		align-items: center;
		flex-wrap: wrap;
	}
	.rectangleRight image{
		width: 30upx;
		height: 30upx;
	}
	.rectangleRightBig{
		display: flex;
		align-items: center;
		height: 50upx;
		line-height: 50upx;
		margin-right: 10upx;
	}
	.rectangleRight .rectangleRightBig image{
		width: 36upx;
		height: 36upx;
	}
	.rectangleRightFooter{
		width: 340upx;
		display: flex;
		justify-content: start;
		align-items: center;
		flex-wrap: nowrap;
	}

	.text{
		display: flex;
		align-items: center;
		height: 50upx;
		line-height: 50upx;
	}
	.text image,.rectangleRightBig image{
		margin-right: 10upx;
	}
	.rectangleBox:nth-child(1){
		background:#07EE14;
	}
	.rectangleBox:nth-child(2){
		background:#120DB5;
	}
	.rectangleBox:nth-child(3){
		background:#A814D2;
	}
</style>
