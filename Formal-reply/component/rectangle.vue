<template>
	<view class="rectangle">
		<view v-for="(item,index) in dataList" :key="index">
			<view class="rectangleLeft">
				
			</view>
			<view class="rectangleRight">
				
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
</style>
