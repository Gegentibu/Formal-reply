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
		<view class="" style="height: 100upx;">
			
		</view>
		<view class="">
			<expert v-show="filterNum==0?true:false" :dataList="dataList"></expert>
			<expert v-show="filterNum==2?true:false" :dataList="dataList"></expert>
			<activity v-show="filterNum==1?true:false" :dataList="dataList"></activity>
		</view>
	</view>
</template>

<script>
	import RenDropdownFilter from '@/components/ren-dropdown-filter/ren-dropdown-filter.vue'
	
	import expert from '../../../component/expert.vue'
	import activity from '../../../component/activity.vue'
    
	export default {
        components:{
			expert,
			activity,
            RenDropdownFilter
        },
        data() {
            return {
				dataList:[{},{},{}],
                filterData:[
                    [{ text: '综合', value: 0 }, { text: '活动', value: 1 }, { text: '达人', value: 2 }, { text: '咨询', value: 3 }, { text: '产品', value: 4 }, { text: '虚拟', value: 5 }, { text: '项目', value: 6 }]
                ],
                defaultIndex:[2],
				filterNum:2
            }
        },
        onLoad() {

        },
        methods: {
            onSelected(res){
                console.log(222,res[0][0].value)
				this.filterNum = res[0][0].value;
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