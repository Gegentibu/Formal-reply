<template>
	<view class="Hybody">
		<view class="titleText" style="margin-top:30upx;">
			认证管理
		</view>
		<view class="" style="margin: 80upx 0 0 0;">
			<view class="content">
				<view class="nuter">
					<view :class="target==0?'active':''" @click="setIndex" data-index="0">
							实名认证
					 </view>
					<view :class="target==1?'active':''" @click="setIndex" data-index="1">
							职业认证
					 </view>
					 <view :class="target==2?'active':''" @click="setIndex" data-index="2">
					 		商家认证
					  </view>
				</view>
				<swiper 
				:duration="500" 
				:current="thisindex"  
				:data-index='thisindex' 
				@change="toggle"
				:style="swiperHeight"
				circular>
					<swiper-item>
						<view class="shimingRz" style="padding: 0 60upx;">
							<view class="">
								<image style="width: 140upx;height: 140upx;" src="../../../static/img/release.png" mode=""></image>
							</view>
							<view class="HyFlexL">
								真实姓名<input type="text" value="" placeholder="请输入真实姓名" />
							</view>
							<view class="HyFlexL">
								身份证号码<input type="text" value="" placeholder="请输入18位身份证号码" />
							</view>
							<view class="">
								<button type="default" style="background-color: #120DB5;color: #fff;">下一步</button>
							</view>
							<view class="" style="color: #28272D;">
								信息仅用于身份认证提升您的账号和资金安全性
								                昔望保障您的信息安全
							</view>
						</view>
					</swiper-item>
					<swiper-item>
						<view class=""  style="padding: 0 60upx;">
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
									选择职业   
								</view>
								<view class="fabuIpt">
									<view class="uni-form-item uni-column">
										<picker @change="bindPickerChange" :range="array">	
											<label class="">{{array[index]}}</label>		
										</picker>
									</view>
								</view>
							</view>
							<view class="" style="margin-top: 40upx;">
								<view class="fabuLeftText">
									上传职业证明材料
								</view>
								<view class="">
									<upimg></upimg>
								</view>
								<view class="" style="margin-bottom: 20upx;color: #3B3838;">
									备注：上传材料可选：名片、工作证、毕业证、相
									关证书单位盖章证明文件等等。
								</view>
							</view>
							<view class="">
								<button type="default" style="background-color: #120DB5;color: #fff;">下一步</button>
							</view>
						</view>
					</swiper-item>
					<swiper-item>

					</swiper-item>
				</swiper>
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
					target:0,
					swiperHeight:'height:500px',
					thisindex:0,
					dataList:[{},{},{}],
					array:['请选择','中国'],
					index:0,
					imageValue:[]
	            }
	        },
	        onLoad() {
				var that = this;
				const query = uni.createSelectorQuery().in(this);
				query.select('#swiperHeight').boundingClientRect(data => {
					console.log(data.height)
					that.swiperHeight ='height:'+data.height+50+'px';
				}).exec();
	        },
	        methods: {
				bindPickerChange: function(e) {		//改变的事件名
					//console.log('picker发送选择改变，携带值为', e.target.value)   用于输出改变索引值
					this.index = e.target.value			//将数组改变索引赋给定义的index变量
					this.jg=this.array[this.index]		//将array【改变索引】的值赋给定义的jg变量
				//	console.log("籍贯为：",this.jg)		//输出获取的籍贯值，例如：中国
				},
				toggle(e){
						let index = e.detail.current
						this.target = index
				},
				setIndex(e){
					let index = e.currentTarget.dataset.index
					this.thisindex = index
				},
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
	.HyFlexL{
		display: flex;
		justify-content: flex-start;
		align-items: center;
	}
	.fabuList{
		display: flex;
		justify-content: flex-start;
		align-items: center;
		margin: 10upx 0;
		text-align: left;
	}
	.fabuIpt{
		width: 400upx;
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
	.fabuLeftText {
		text-align: left;
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
	.nuter{
		width: 100%;
		height: 80rpx;
		line-height: 80rpx;
		display: flex;
		justify-content: space-around;
	}
	.nuter view{
		/* flex: 1; */
		/* font-size: 30rpx; */
		text-align: center;
		transition: all 0.5s ease .1s;
		/* background-color: #f0f0f0; */
		text-align: left;
		margin-right: 20upx;
		/* font-size: 16px; */
/* 		font-size: 18px;
		font-family: '方正工业黑-标准';
		font-weight: 600; */
	}
	.active{
		box-sizing: border-box;
		/* color: #007AFF; */
/* 		border-bottom: 5rpx solid #00aaff;
		background-color: #f3ffff;
		border-radius: 10rpx;
		box-shadow: 3px 3px 5px #888888; */
		font-size: 20px;
		font-family: '方正工业黑-标准';
		font-weight: 600;
		padding-bottom:5px;
		border-bottom: 2px solid #fff;
	}
/* 	swiper{
		height: 100%;
	} */
	swiper-item{
		width: 100%;
		/* overflow: hidden; */
		text-align: center;
		/* line-height: 300rpx; */
		/* background-color: red; */
	}
	.swiper-item{
		overflow-y: scroll;
		width: 99.5%;
		height: 99%;
		/* background-color: white; */
		/* height: 99%; */
		box-sizing: border-box;
		padding: 1rpx;
	}
	.shimingRz{
		font-size: 16px;
	}
	.shimingRz view {
		margin: 40upx 0;
	}
</style>