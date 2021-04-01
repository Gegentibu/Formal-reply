<template>
	<view class="Hybody">
		<view class="titleText">
			我的收藏
		</view>
		<view class="" style="margin: 40upx 0;">
			<view class="releaseBj" @click="goToZx">
				<text class="releaseBjTitle">让好产品走出去让更多人购买</text>
				<text class="releaseBjText">在这里您可以出售您公司或代理产品及朋友的产品来互动营销，让指尖生意源源不断的继续。</text>
			</view>
		</view>
		<view class="" style="margin: 40upx 0;">
			<view class="releaseBj" @click="goToZx">
				<text class="releaseBjTitle">让好产品走出去让更多人购买</text>
				<text class="releaseBjText">在这里您可以出售您公司或代理产品及朋友的产品来互动营销，让指尖生意源源不断的继续。</text>
			</view>
		</view>
	</view>
</template>

<script>
	import RenDropdownFilter from '@/components/ren-dropdown-filter/ren-dropdown-filter.vue'
	    export default {
	        components:{
	            RenDropdownFilter
	        },
	        data() {
	            return {
	                filterData:[
	                    [{ text: '城市', value: '' }, { text: '北京', value: 1 }, { text: '上海', value: 2 }, { text: '深圳', value: 3 }],
	                    [{ text: '种类', value: '' }, { text: '亲自', value: 1 }, { text: '互联网', value: 2 }, { text: '创业', value: 3 }],
	                    [{ text: '日期', value: '' }, { text: '近一周', value: 1 }, { text: '近一个月', value: 2 }, { text: '近三个月', value: 3 }],
	                    [{ text: '距离', value: '' }, { text: '5公里内', value: 1 }, { text: '10公里内', value: 2 }, { text: '20公里内', value: 3 }],
	                    [{ text: '价格', value: '' }, { text: '免费', value: 1 }, { text: '1-100元', value: 2 }, { text: '101-200元', value: 3 }]
	                ],
	                defaultIndex:[0,0,0,0,0,]
	            }
	        },
	        onLoad() {
				
	        },
	        methods: {
	            onSelected(res){
	                console.log(res)
	            },
	            dateChange(d){
	               uni.showToast({
	                   icon:'none',
	                   title:d
	               })
	            }
	        }
	    }
</script>

<style scoped>
	.Hybody{
		padding: 0 32upx;
		padding-top: 50upx;
		height: 1500upx;
		font-size: 14px;
		background-color: #080808;
		color: #fff;
		text-align: left;
	}
	.titleText{
		color: rgba(255, 255, 255, 100);
		font-size: 22px;
		text-align: left;
		font-weight: 600;
		font-family: 方正工业黑-标准;
		/* margin: 40upx 0; */
		position: fixed;
		width: 100%;
		left: 30upx;
		height: 80upx;
		line-height: 80upx;
		background-color: #080808;
		top: 0;
	}
	.miList{
		display: flex;
		justify-content: space-between;
		align-items: center;
		margin: 30upx 0;
		color:rgba(153, 155, 178, 100);
	}
	.tijiao{
		width: 304upx;
		height: 63upx;
		line-height: 63upx;
		border-radius: 25upx;
		background-color: rgba(149, 70, 232, 100);
		color: rgba(255, 255, 255, 100);
		font-size: 14px;
		text-align: center;
		font-family: Microsoft Yahei;
	}
	image {
		width: 250upx;
		height: 250upx;
	}
	.HyFlexC{
		display: flex;
		justify-content: center;
		align-items: center;
	}
	.c-flex-align {
		justify-content: center;
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
	.root{
		margin-top: 30rpx;
	}
</style>