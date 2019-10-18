<template>
	<view class="content">
		<view  v-bind:style="{ color: vColor, fontSize: fontSize + 'px' }">666</view>
		<!--background-color写成backgroundColor-->
		<view  v-bind:style="{color:colorObj.color,
		fontSize:colorObj.fontSize,
		backgroundColor:colorObj.background_color }"
		style="text-decoration: line-through;">2222ddd</view>
	</view>
</template>

<script>
	//红色
	var c_red='#E22018';
	//蓝色
	var c_blue='#3984FF';
	//绿色
	var c_green='#1AA034'
	//橙色
	var c_orange='#FD5C2D'
	//黑色
	var c_black='#000000';
	var _this;
	//引入js報錯
	// import  { colors } from '../../static/colors.js';
	export default {
		data() {
			return {
				vColor:'#C95941',
				fontSize:20,
				colorObj:{ color:c_red , fontSize: '20px',background_color:c_blue },
				}
		},
		onReady() {
			//初始化this对象
			_this=this;
			setTimeout(function() {
				//3秒钟改成黑色背景
				_this.colorObj.background_color=c_black;
				//3秒后字体=40px
				_this.colorObj.fontSize='40px';
			}, 1000*3);
		},
		methods: {

		}
	}
</script>

<style>
	.content {
		width: 100%;
		height: 500rpx;
		display: flex;
		flex-direction: column;
	}
</style>
