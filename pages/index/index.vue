<template>
	<view class="content">
		
		<view v-if="1==2">1==2</view>
		<view v-else>数字判断 进入else</view>
		<view v-if='"李四"==李四'>汉字判断李四</view>
		<view v>王五</view>
	</view>
</template>

<script>
	const xyl_name = 'http://uniapp.dcloud.io';  
	
	//当前页面对象
	var _this;
	export default {
		data() {
			return {
				boo:true,
				arr1:[{'name':'张三','age':45},{'name':'李四','age':23}],
			}
		},
		onReady() {
			全局变量.webViewUrl
		},
		methods: {

		}
	}
</script>

<style>
	.content {
		width: 100%;
		height: 500rpx;
		display: flex;/*默认主轴是横向布局*/
		flex-direction: column;
	}

	
</style>


