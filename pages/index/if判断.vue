<template>
	<view class="content">
		<!-- if else -->
		<view v-if="1==2">1==2</view>
		<view v-else>数字判断 进入else</view>
		<!-- if else -->
		<view v-if='"李四"==李四'>汉字判断 进入if</view>
		<view v-else>王五</view>
		<!-- if else if-->
		<view v-if="num==1">进入if</view>
		<view v-else="num==2">进入else</view>
		<view  v-else-if="num==3">进入v-elseif</view>
		<!-- 方法返回值判断-->
		<view v-if="'张三'==getStr(10)">张三</view>
		<view v-else="'李四'==getStr(2)">李四</view>
		<view v-else="'王五'==getStr(30)">王五</view>
	</view>
</template>

<script>
	//当前页面对象
	var _this;
	export default {
		data() {
			return {
				num:3,
			}
		},
		methods: {
			getStr(num){
				if (1==num) {
					return "张三"
				}else if (2==num) {
					return "李四"
				}
				return "王五";
			}
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


