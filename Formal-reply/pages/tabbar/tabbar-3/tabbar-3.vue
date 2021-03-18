<template>
	<view class="Hybody">
		<view class="">
			<image class="fabuImg" src="../../../static/tu.jpg" mode=""></image>
		</view>
		<view class="fabuContent">
			<view class="fabuTitle">
				发布活动信息
			</view>
			<view class="fabuList">
				<view class="fabuLeftText">
					活动简介
				</view>
				<view class="fabuIpt">
					<input type="text" placeholder="请输入活动简称不要超过10个字">
				</view>
			</view>
			<view class="fabuList">
				<view class="fabuLeftText">
					活动主题
				</view>
				<view class="fabuIpt">
					<input type="text" placeholder="请输入活动简称不要超过10个字">
				</view>
			</view>
			<view class="fabuList">
				<view class="fabuLeftText">
					活动行业
				</view>
				<view class="fabuIpt">
					<view class="uni-form-item uni-column">
						<picker @change="bindPickerChange" :range="array">	
							<label class="">{{array[index]}}</label>		
						</picker>
					</view>
				</view>
			</view>
			<view class="fabuList">
				<view class="fabuLeftText">
					行业细分
				</view>
				<view class="fabuIpt">
					<view class="uni-form-item uni-column">
						<picker @change="bindPickerChange" :range="array">	
							<label class="">{{array[index]}}</label>		
						</picker>
					</view>
				</view>
			</view>
			<view class="fabuList">
				<view class="fabuLeftText">
					活动强度
				</view>
				<view class="fabuIpt" style="width: 300upx;">
					<view class="uni-form-item uni-column">
						<picker @change="bindPickerChange" :range="array">	
							<label class="">{{array[index]}}</label>		
						</picker>
					</view>
				</view>
				<view style="width: 100upx;margin-left: 30upx;">
					星
				</view>
			</view>
			<view class="fabuList">
				<view class="fabuLeftText">
					开始日期
				</view>
				<view class="fabuIpt" style="width: 300upx;">
					<!-- <uni-datetime-picker></uni-datetime-picker> -->
					<!-- <uni-datetime-picker v-model="vModelDatetime" start="2010-6-10 08:30:30" end="2021-6-10 08:30:30"></uni-datetime-picker> -->
					<!-- <uni-datetime-picker :value="timestamp" return-type="timestamp" start="1276129830000" end="1623285030000" @change="timestampChange"></uni-datetime-picker> -->
					<uni-datetime-picker type="date" :value="date" start="2020-6-15" end="2025-6-15" @change="dateChange"></uni-datetime-picker>
					<!-- <uni-datetime-picker type="time" :value="time" start="06:30:30" end="12:30:30" @change="timeChange"></uni-datetime-picker> -->
				</view>
			</view>
			<view class="fabuList">
				<view class="fabuLeftText">
					结束日期
				</view>
				<view class="fabuIpt" style="width: 300upx;">
					<!-- <uni-datetime-picker></uni-datetime-picker> -->
					<!-- <uni-datetime-picker v-model="vModelDatetime" start="2010-6-10 08:30:30" end="2021-6-10 08:30:30"></uni-datetime-picker> -->
					<!-- <uni-datetime-picker :value="timestamp" return-type="timestamp" start="1276129830000" end="1623285030000" @change="timestampChange"></uni-datetime-picker> -->
					<uni-datetime-picker type="date" :value="date" start="2020-6-15" end="2025-6-15" @change="dateChange"></uni-datetime-picker>
					<!-- <uni-datetime-picker type="time" :value="time" start="06:30:30" end="12:30:30" @change="timeChange"></uni-datetime-picker> -->
				</view>
			</view>
			<view class="fabuList">
				<view class="fabuLeftText">
					集合时间
				</view>
				<view class="fabuIpt" style="width: 300upx;">
					<!-- <uni-datetime-picker></uni-datetime-picker> -->
					<!-- <uni-datetime-picker v-model="vModelDatetime" start="2010-6-10 08:30:30" end="2021-6-10 08:30:30"></uni-datetime-picker> -->
					<!-- <uni-datetime-picker :value="timestamp" return-type="timestamp" start="1276129830000" end="1623285030000" @change="timestampChange"></uni-datetime-picker> -->
					<!-- <uni-datetime-picker type="date" :value="date" start="2020-6-15" end="2025-6-15" @change="dateChange"></uni-datetime-picker> -->
					<uni-datetime-picker type="time" :value="time" start="06:30:30" end="12:30:30" @change="timeChange"></uni-datetime-picker>
				</view>
			</view>
			<view class="fabuList">
				<view class="fabuLeftText">
					关于费用
				</view>
				<view class="fabuIpt"  style="display: flex;justify-content: start;align-items: center;">
					<view class="" style="width: 200upx;">
						<input type="text" placeholder="请输入活动简称不要超过10个字">
					</view>
					<view class="" style="width: 100upx;">
						元/每人
					</view>
					<view class="" style="width: 100upx;">
						免费
					</view>
				</view>
			</view>
			<view class="fabuList">
				<view class="fabuLeftText">
					活动简介
				</view>
				<view class="fabuIpt">
					<input type="text" placeholder="请输入活动简称不要超过10个字">
				</view>
			</view>
			<view class="fabuList">
				<view class="fabuLeftText">
					适宜人群
				</view>
				<view class="fabuIpt">
					<input type="text" placeholder="请输入活动简称不要超过10个字">
				</view>
			</view>
			<view class="fabuList">
				<view class="fabuLeftText">
					联系人员
				</view>
				<view class="fabuIpt">
					<input type="text" placeholder="请输入活动简称不要超过10个字">
				</view>
			</view>
			<view class="fabuList">
				<view class="fabuLeftText">
					联系电话
				</view>
				<view class="fabuIpt">
					<input type="text" placeholder="请输入活动简称不要超过10个字">
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	import uniDatetimePicker from '@/components/uni-datetime-picker/uni-datetime-picker.vue'
	export default {
		components: {uniDatetimePicker},
		data() {
			return {
				title: 'Hello',
				array:['请选择','中国'],
				index:0
			}
		},
		onLoad() {

		},
		methods: {
			goToFbdt(){
				uni.navigateTo({
					url: '/pages/tabbar/tabbar-3/fabiaodongtai',
				});
			},
			bindPickerChange: function(e) {		//改变的事件名
				//console.log('picker发送选择改变，携带值为', e.target.value)   用于输出改变索引值
				this.index = e.target.value			//将数组改变索引赋给定义的index变量
				this.jg=this.array[this.index]		//将array【改变索引】的值赋给定义的jg变量
			//	console.log("籍贯为：",this.jg)		//输出获取的籍贯值，例如：中国
			},
		}
	}
</script>

<style>
	.Hybody{
		/* padding: 0 32upx; */
		height: 100%;
		font-size: 12px;
		background-color: #080808;
		color: #fff;
	}
	.fabuImg{
		width: 100%;
		height:500upx;
	}
	.fabuContent{
		position: relative;
		z-index: 1;
		top: -200upx;
		border-top-left-radius: 50upx;
		border-top-right-radius: 50upx;
		min-height: 500upx;
		background-color: #080808;
		padding:70upx 88upx 0 88upx ;
	}
	.fabuTitle{
		text-align: center;
		font-family: 方正新书宋-标准;
		font-size: 24px;
		margin-bottom: 70upx;
	}
	.fabuList{
		display: flex;
		justify-content: flex-start;
		align-items: center;
		margin: 10upx 0;
	}
	.fabuLeftText{
		font-size: 16px;
		font-weight: 400;
		margin-right: 30upx;
	}
	.fabuIpt{
		width: 400upx;
	}
	.fabuIpt input{
		    border-radius: 5px;
		    padding: 3px 0px;
		    box-sizing: border-box;
		    cursor: pointer;
	}
	.uni-column{
		background-color: #fff;
		color: #000000;
		/* text-align: right; */
		border: 1px solid #E5E5E5;
		    border-radius: 5px;
		    padding: 3px 10px;
		    box-sizing: border-box;
		    cursor: pointer;
	}
</style>
