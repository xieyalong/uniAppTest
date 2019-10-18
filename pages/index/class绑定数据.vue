<template>
	<view>
	<view class="content">
		<view 
		class="v" 
		v-for="(item,index) in menus" 
		v-bind:class="[select_index==index?'select':'defult']"
		@click="menuClick(index)">
			{{item}}
		</view>
	</view>
	<view>当前选择:{{selectValue}}</view>
	</view>
</template>

<script>
	var _this;
	export default {
		data() {
			return{
				//默认选择的
				select_index:0,
				menus:['新闻','汽车','读书'],
				selectValue:''
			}
		}
		,onLoad() {
			_this=this;
			_this.selectValue=_this.menus[_this.select_index];
		}
		,methods:{
			menuClick:function(index){
				//更换选择项
				_this.select_index=index;
				_this.selectValue=_this.menus[_this.select_index];
				console.log(_this.menus[index]);
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
	/* 权重 */
	.v{
		flex: 1;
		text-align: center;
	}
	
	/* 选中的颜色 */
	.select{
		color: #007AFF;
	}
	/* 默认的颜色 */
	.defult{
	 color: #2C405A;
	}
</style>
