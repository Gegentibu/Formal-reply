<template>
	<view class="Hybody">
		<view class="fabuContent">
			<view class="titleText">
				主页设置
			</view>
			<view class="" style="margin-top: 40upx;">
				<view class="fabuLeftText">
					我的照片
				</view>
				<view class="">
					<upimg></upimg>
				</view>
				<view class="" style="margin-bottom: 20upx;color: #3B3838;">
					个人照片上传尺寸最适宜400*400像素的正方形 照
					片为效果最佳。
				</view>
			</view>
			<view class="" style="margin-bottom: 20upx;">
				<view class="fabuLeftText">
					人生格言
				</view>
				<view class="">
					<textarea style="background: #fff;margin-top: 20upx;height: 140upx;" value="" placeholder="请输入格言，文字必须12到20个字中间，不然系统不会推送到首页达人展示。" />
				</view>
				<view class="">
					
				</view>
			</view>
			<view class="" style="margin-bottom: 20upx;">
				<view class="fabuLeftText">
					我的介绍
				</view>
				<view class="">
					<textarea style="background: #fff;margin-top: 20upx;height: 140upx;" value="" placeholder="请输入个人介绍，文字最少50个字最多200字之内不然系统 不会推送到首页达人展示。" />
				</view>
				<view class="">
					
				</view>
			</view>
			<view class="fabuLeftText">
				名片信息
			</view>
			<view class="fabuList">
				<view class="fabuLeftText">
					选择行业
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
					职业选择
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
					单位名称
				</view>
				<view class="fabuIpt">
					<input type="text" placeholder="请输入活动简称不要超过10个字">
				</view>
			</view>
			<view class="fabuList">
				<view class="fabuLeftText">
					职　　务
				</view>
				<view class="fabuIpt">
					<input type="text" placeholder="请输入活动简称不要超过10个字">
				</view>
			</view>
			<view class="fabuList">
				<view class="fabuLeftText">
					手机号码
				</view>
				<view class="fabuIpt">
					<input type="text" placeholder="请输入活动简称不要超过10个字">
				</view>
			</view>
			<view class="fabuList">
				<view class="fabuLeftText">
					单位地址
				</view>
				<view class="fabuIpt">
					<input type="text" placeholder="请输入活动简称不要超过10个字">
				</view>
			</view>
			<view class="" style="margin-bottom: 20upx;">
				<view class="fabuLeftText">
					单位业务
				</view>
				<view class="">
					<textarea style="background: #fff;margin-top: 20upx;height: 140upx;" value="" placeholder="请输入个人介绍，文字最少50个字最多200字" />
				</view>
				<view class="">
					
				</view>
			</view>
			<view class="" style="margin-top: 40upx;">
				<view class="fabuLeftText">
					我的照片
				</view>
				<view class="">
					<upimg></upimg>
				</view>
				<view class="" style="color: #3B3838;">
					个人主页就是您的社交名片，完善个人主页平台才会
					把个人主页信息不定时推送到首页达人名片组内，您
					需要让更多的人认识你或需要宣传推广您的公司、项
					目、产品及更多服务，请完善您的主页信息。
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	import uniDatetimePicker from '@/components/uni-datetime-picker/uni-datetime-picker.vue'
	import upimg from '../../../component/sunui-upimg.vue'
	export default {
		components: {uniDatetimePicker,upimg},
		data() {
			return {
				title: 'Hello',
				array:['请选择','中国'],
				index:0,
				imageValue:[]
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
	.titleText{
		color: rgba(255, 255, 255, 100);
		font-size: 22px;
		text-align: left;
		font-weight: 600;
		font-family: 方正工业黑-标准;
		/* margin: 40upx 0; */
		width: 100%;
		left: 30upx;
		height: 80upx;
		line-height: 80upx;
		background-color: #080808;
	}
	.fabuContent{
		/* position: relative; */
		z-index: 1;
		/* top: -200upx; */
		border-top-left-radius: 50upx;
		border-top-right-radius: 50upx;
		min-height: 500upx;
		background-color: #080808;
		padding:70upx 88upx 80upx 88upx ;
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
	.fabuDitu image{
		width: 100%;
		height: 430upx;
	}
</style>
