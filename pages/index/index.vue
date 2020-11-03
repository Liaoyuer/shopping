<template>
	<view class="homepage">
		<view class="page-header">
			<view class="top width-90 flex justify-between">
				<view class="local flex justify-between">
					<image src="../../static/images/home/weizhi.png" mode=""></image>
					<text>我的位置</text>
				</view>
				<view class="weather flex justify-between">
					<image src="../../static/images/weather/duoyun.png" mode=""></image>
					<text>多云 /21℃</text>
				</view>
			</view>
			<view class="width-90 search-bar flex justify-between">
				<input class="" type="text" value="" placeholder="搜索关键词" />
				<image src="../../static/images/home/search.png" mode=""></image>
			</view>
			<view class="">
				<u-swiper :list="list"></u-swiper>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {}
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style lang="scss">
	.width-90{
		width: 94%;
		margin: 0 auto;
	}
	.homepage{
		width: 750rpx;
		height: 100%;
		background-color: red;
		.page-header{
			height: 514rpx;
			background: #fa5376;
			background-image: linear-gradient(#fa5376, #fff);
			.top{
				padding-top: 20rpx;
				color: #fff;
				font-size: 16rpx;
				image{
					width: 35rpx;
					height: 35rpx;
					margin-right: 10rpx;
				}
			}
			.search-bar{
				height: 60rpx;
				border-radius: 20px;
				margin-top: 25rpx;
				background-color: #fff;
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
		}
	}
</style>
