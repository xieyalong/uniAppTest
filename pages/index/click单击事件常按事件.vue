<template>
	<view>
	<view class="content">
		<view id="90" data="aaa" @click="clickTest" @longtap="longtapTest('你好')"
		style="background-color: #8F8F94;width: 200rpx;height: 200rpx;">
			<view id="20"
			style="width: 100rpx;height: 100rpx;background-color: #007AFF;">小块</view>
			大块
		</view>
	</view>
	</view>
</template>

<script>
	var _this;
	export default {
		data() {
			return{
			}
		}
		,onLoad() {
			_this=this;
		}
		,methods:{
			clickTest:function(e){
				//事件绑定的view id="90" 运行两遍，可能有多少子控件就触发多少个事件
				console.log(e.currentTarget.id);
				//整个元素的view id="90"和<view id="20"，运行两遍
				console.log(e.target.id);
				//吐司
			uni.showToast({
				title:'內容'+e.currentTarget.id,
			});
			},
			longtapTest:function(str){
				console.log(str);
				//弹出框
				uni.showModal({
					content: '触发常按事件，str='+str,
					showCancel: false
				});
			}
		}
	}
</script>

<style>
	.content {
		width: 100%;
		height: 100rpx;
		display: flex;
		
	}
	
</style>
