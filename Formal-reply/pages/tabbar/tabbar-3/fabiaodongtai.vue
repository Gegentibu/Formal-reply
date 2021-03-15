<template>
	<view class="Hybody">
		<textarea class="textarea" value="" placeholder="这一刻你的想法" />
		<upimg></upimg>
	</view>
</template>

<script>
	import upimg from '../../../component/sunui-upimg.vue'
	export default {
	    components:{
			upimg
	    },
	    data() {
	        return {}
			}
	}
</script>
<style>
	.Hybody{
		padding: 12upx 32upx;
		height: 1445upx;
		background-color: #080808;
		color: #fff;
	}
	.textarea{
		width: 100%;
	}
</style>
