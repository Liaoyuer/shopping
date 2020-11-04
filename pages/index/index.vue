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
			<view class="swiper">
				<u-swiper :list="list" :effect3d="true" height="340" border-radius="20" bg-color="none"></u-swiper>
			</view>
		</view>
		<view class="goods-classify width-90">
			
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				list: [
					'https://ss2.bdstatic.com/70cFvnSh_Q1YnxGkpoWK1HF6hhy/it/u=339984553,3509384023&fm=26&gp=0.jpg',
					'https://ss3.bdstatic.com/70cFv8Sh_Q1YnxGkpoWK1HF6hhy/it/u=1786439814,215205363&fm=26&gp=0.jpg',
					'https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1600399666309&di=3670afbef52571b71b98f4562043498e&imgtype=0&src=http%3A%2F%2Fpic1.win4000.com%2Fwallpaper%2F8%2F57ea3c2d57be6.jpg'
				]
			}
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
		background-color: pink;
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
			.swiper{
				padding: 20rpx 0;
				height: 356rpx;
				background: rgba(0,0,0,0);
			}
		}
		.goods-classify{
			height: 361rpx;
			margin-top: 20rpx;
			box-shadow: 0px 0px 5px #eee;
			border-radius: 10rpx;
			background: #fff;
		}
	}
</style>
