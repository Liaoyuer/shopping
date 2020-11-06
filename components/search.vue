<template>
	<view class="search-bar flex justify-between">
		<input class="" type="text" value="" placeholder="搜索关键词" />
		<image src="../static/images/home/search.png" mode=""></image>
	</view>
</template>

<script>
</script>

<style lang="scss">
	.search-bar{
		height: 60rpx;
		border-radius: 20px;
		margin-top: 25rpx;
		background: #f5f5f5;
		padding: 0 35rpx;
		box-sizing: border-box;
		image{
			width: 40rpx;
			height: 40rpx;
			padding-top: 10rpx;
			display: block;
		}
		input{
			width: 80%;
			height: 60rpx;
			font-size: 18rpx;
		}
		// width: 94%;
	}
</style>
