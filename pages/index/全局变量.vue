<template>
	<view class="content">
		<view>---{{name}}</view>
	</view>
</template>

<script>
	// import c from '../../common/colors.js'
	export default {
		data() {
			return {
				name:'sss'
				}
		},
		onReady() {
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
