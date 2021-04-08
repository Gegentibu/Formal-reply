<template>
	<view class="Hybody">
		<view class="titleText" style="margin-top:30upx;">
			建团奖励规则
		</view>
		<view class="">
			1、您邀请的人按注册时间顺序每两个人按排给您一个
			团，进团的两个人邀请的人同样按注册时间顺序系统
			按两个人按排到您的团，7个人全部到起就算建团成功。
		</view>
		<view class="">
			2、团成员成为付费会员平台会根据购买的会员级别金
			额一定比例给予每一个团成员推广奖励。
		</view>
		<view class="">
			3、推广奖励金额在成团前以待结算奖励金额存在，当
			7人团人数到起，系统会自动发放到您的推广收入里。
		</view>
		<view class="">		
			4、团推广奖励区别于邀请奖励的额外奖励。
		</view>
		<view class="">
			5、奖励比例白银会员25%、黄金会员20%、铂金会员
			15%、钻石会员15%、粉钻会员15%、黑钻会员15%比
			例团队成员均摊尊享。
		</view>
	</view>
</template>

<script>
	    export default {
	        data() {
	            return {
					target:0,
					swiperHeight:'height:500px',
					thisindex:0,
					dataList:[{},{},{}],
					data:[{},{}]
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
	.HyFlexB{
		display: flex;
		justify-content: space-between;
		align-items: center;
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
	
	.Hybody view{
		margin: 30upx 0;
	}

</style>