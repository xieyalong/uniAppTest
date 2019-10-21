<template>
	<view class="content">
		<!--
		scroll-y="true";
		-->
		<scroll-view class="scv"
		scroll-x="true">
		 <view id="demo1" class="scroll-view-item uni-bg-red">A</view>
		 <view id="demo2" class="scroll-view-item uni-bg-green">B</view>
		 <view id="demo3" class="scroll-view-item uni-bg-blue">C</view>
		 <view id="demo3" class="scroll-view-item uni-bg-blue">d</view>
		 <view id="demo3" class="scroll-view-item uni-bg-blue">e</view>
		</scroll-view>
	</view>
</template>

<script>
	var _this;
	export default {
		data() {
			return{
				size:100,
			}
		}
		,onLoad() {
			_this=this;
		}
		,methods:{
		}
	}
</script>

<style>
	/* 
	如果是scroll-x="true"，横向滚动，需要
	scroll-view（display: flex;），
	里面的子元素（display: inline-block;）
	 */

scroll-view（）{
	display: flex;
}
scroll-view view{
	display: inline-block;
}
	.scv{
		/*高度会占满整个屏幕  */
		width: 100%;
		margin: 0 auto;
		height: 100%;
		/* -------------- */
		background-color: #8F8F94;
		
	}
	.scv view{
		width: 50%;
		height: 200rpx;
		background-color: #4CD964;
		
	}
	/* .item{
		background-color: #007AFF;
		margin-top: 1rpx;
		width: 100%;
		height: 50rpx;
	} */
</style>
