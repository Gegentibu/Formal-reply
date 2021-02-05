<template>
	<view class="expert">
		<view class="expertBox" v-for="(item,index) in dataList" :key="index">

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
