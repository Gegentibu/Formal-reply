<template>
	<view class="Hybody">
		<view class="root">
			<ren-dropdown-filter :filterData='filterData' :defaultIndex='defaultIndex'
			@onSelected='onSelected' @dateChange='dateChange'></ren-dropdown-filter>
		</view>
		<view class=" title">
			<view></view>
			<view class="titleText">
				答复CBD中心
			</view>
			<view>
				<image class="sousuo" src="../../../static/img/tabbar/guanzhuactive.png" mode=""></image>
			</view>
		</view>
		<view class="" style="height: 130upx;">
			
		</view>
		<view class="">
			<expert :dataList="dataList"></expert>
		</view>
	</view>
</template>

<script>
	import RenDropdownFilter from '@/components/ren-dropdown-filter/ren-dropdown-filter.vue'
	
	import expert from '../../../component/expert.vue'
    
	export default {
        components:{
			expert,
            RenDropdownFilter
        },
        data() {
            return {
				dataList:[{},{},{}],
                filterData:[
                    [{ text: '综合', value: '' }, { text: '活动', value: 1 }, { text: '达人', value: 2 }, { text: '咨询', value: 3 }]
                ],
                defaultIndex:[0]
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

<style>
	.Hybody{
		padding: 0 32upx;
		height: 100%;
		font-size: 12px;
		background-color: #080808;
		color: #fff;
	}
		
	.root{
		background-color: #080808;
	}
	.title{
		width: 70%;
		margin-left: 15%;
		display: flex;
		justify-content: space-between;
		align-items: center;
		height: 108upx;
		z-index: 9999;
		position: fixed;
		left: 0;
		background-color: #080808;
	}
	.titleText{
		font-family: 方正工业黑-标准;
		font-size: 20px;
		font-weight: 600;
	}
	.sousuo{
		width: 50upx;
		height: 50upx;
	}
</style>