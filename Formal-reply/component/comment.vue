<template>
	<view class="comment">
		<view class="HyFlexB">
			<view class="">
				
			</view>
			<view class="">
				321条评论
			</view>
			<view class="">
				×
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
	.comment{
		width: 750upx;
		background-color: #28272D;
		position: fixed;
		bottom: 0;
		height: 650upx;
		border-top-left-radius: 20upx;
		border-top-right-radius: 20upx;
	}
	.HyFlexB{
		display: flex;
		justify-content: space-between;
		align-items: center;
	}
</style>
