<template>
	<view class="Hybody">
		<view class="">
			<image class="fabuImg" src="../../../static/tu.jpg" mode=""></image>
		</view>
		<view class="fabuContent">
			<view class="fabuTitle">
				发布产品信息
			</view>
			<view class="fabuList">
				<view class="fabuLeftText">
					产品名称
				</view>
				<view class="fabuIpt">
					<input type="text" placeholder="请输入活动简称不要超过10个字">
				</view>
			</view>
			<view class="fabuList">
				<view class="fabuLeftText">
					产品大类
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
					产品小类
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
					产品规格
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
					是否包邮
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
					产品价格
				</view>
				<view class="fabuIpt">
					<input type="text" placeholder="请输字入16字以内适宜人群描述">
				</view>
			</view>
			<view class="fabuList">
				<view class="fabuLeftText">
					固定运费
				</view>
				<view class="fabuIpt">
					<input type="text" placeholder="请输入联系人姓名">
				</view>
			</view>
			<view class="fabuList">
				<view class="fabuLeftText">
					联系电话
				</view>
				<view class="fabuIpt">
					<input type="text" placeholder="请输入联系人电话号">
				</view>
			</view>
			<view class="fabuList">
				<view class="fabuLeftText">
					产品描述
				</view>
				<view class="fabuIpt">
					<input type="text" placeholder="请输入活动地点信息">
				</view>
			</view>
			<view class="" style="margin-top: 100upx;">
				<view class="fabuLeftText">
					产品海报
				</view>
				<view class="">
					<upimg></upimg>
				</view>
				<view class="" style="margin-bottom: 20upx;color: #3B3838;">
					备注：产品海报图会展示在首页和产品详情的头部尺寸为正方形，800*800像素为最适宜图片，不合格图片的产品会被驳回。
				</view>
			</view>
			<view class="" style="margin-bottom: 20upx;">
				<view class="fabuLeftText">
					产品详情
				</view>
				<view class="">
					<textarea style="background: #fff;margin-top: 20upx;" value="" placeholder="1、请输入文字内容，需要中间上传图片或视频请点击下方上传按钮。2、照片上传目前支持jpg和png格式，每一张图片大小不能超过5MB。3、视频目前只支持上传一个，格式支持MP4、MOV大小不能超过30MB。" />
				</view>
				<view class="">
					
				</view>
			</view>
			<view class="">
				<view class="fabuLeftText">
					合规证明材料
				</view>
				<view class="">
					<upimg></upimg>
				</view>
				<view class="" style="margin-bottom: 20upx;color: #3B3838;">
					备注：产品合规证明材料指产品生产厂家营业执照或检测报告、合格证等等能够证明产品合理合法合规即可。
				</view>
			</view>
			<view class="fabuList" style="flex-wrap: wrap;">
				<view class="fabuLeftText" style="width: 100%;">
					推广分润
				</view>
				<view class="" style="width: 100%;margin: 20upx 0 6upx 0;">
					<view class="uni-form-item uni-column">
						<picker @change="bindPickerChange" :range="array">	
							<label class="">{{array[index]}}</label>		
						</picker>
					</view>
				</view>
				<view class="" style="width: 100%;margin-bottom: 20upx;color: #3B3838;">
					注；分润为成交额的百分比，请谨慎计算选择。
				</view>
			</view>
			<view class="fabuList" style="flex-wrap: wrap;">
				<view class="fabuLeftText" style="width: 100%;">
					一级推广分润比例
				</view>
				<view class="" style="width: 100%;margin: 20upx 0 6upx 0;">
					<view class="uni-form-item uni-column">
						<picker @change="bindPickerChange" :range="array">	
							<label class="">{{array[index]}}</label>		
						</picker>
					</view>
				</view>
			</view>
			<view class="fabuList" style="flex-wrap: wrap;">
				<view class="fabuLeftText" style="width: 100%;">
					一级推广分润比例
				</view>
				<view class="" style="width: 100%;margin: 20upx 0 6upx 0;">
					<view class="uni-form-item uni-column">
						<picker @change="bindPickerChange" :range="array">	
							<label class="">{{array[index]}}</label>		
						</picker>
					</view>
				</view>
			</view>
			<view class="" style="display: flex;justify-content: center;align-items: center;flex-wrap: wrap;">
				<view class="" style="font-size: 24px;font-weight: 600;text-align: center;margin:100upx 0 30upx 0;">
					答复团队非常感谢您的支持
				</view>
				<view class="" style="width:400upx;padding: 20upx 10upx;border-radius: 40upx;background-color: #fff;text-align: center;color: #000000;">
					提交
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
	.fabuDitu image{
		width: 100%;
		height: 430upx;
	}
</style>
