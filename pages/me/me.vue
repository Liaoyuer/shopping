<template>
	<view class="me-page">
		<view class="user-header">
			<view class="user-info flex">
				<view class="avatar">
					<image src="/static/images/face.jpg" mode=""></image>
				</view>
				<text>用户2020</text>
			</view>
			<view class="card">
				<view class="flex justify-between">
					<view class="flex">
						<u-icon name="integral" color="#f6e5a3" size="42"></u-icon>
						<text class="vip-text">商城尊享会员</text>
					</view>
					<view class="">
						<u-button class="custom-style" shape="circle" :hair-line="false" size="mini">钻石会员</u-button>
					</view>
				</view>
				<view class="banquan">
					商城版权所有©
				</view>
			</view>
		</view>
		<view class="all-order width-90">
			<view class="all-order-top flex justify-between">
				<view>
					<text class="order-icon iconfont icon-icon-"></text>
					<text class="all-order-text">全部订单</text>
				</view>
				<image src="/static/images/home/right.png" mode=""></image>
			</view>
			<u-grid :col="5">
				<u-grid-item v-for="(item,index) in orderText" :key="item.id">
					<text class="iconfont" :class="item.icon"></text>
					<text class="grid-text">{{item.name}}</text>
				</u-grid-item>
			</u-grid>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				orderText: [{
				  name: '待付款',
				  icon: 'icon-daifukuan',
				  url: '',
				  id: 0
				}, {
				  name: '待发货',
				  icon: 'icon-daifahuo',
				  url: '',
				  id: 1
				}, {
				  name: '待收货',
				  icon: 'icon-daishouhuo1',
				  url: '',
				  id: 2
				},
				{
				  name: '待评价',
				  icon: 'icon-daipingjia',
				  url: '',
				  id: 3
				},{
				  name: '退款/售后',
				  icon: 'icon-shouhou',
				  url: '/pages/views/order/afterSaleList',
				  id: 4
				}]
			}
		},
		methods: {
			
		}
	}
</script>

<style lang="scss">
	.me-page{
		background: #f8f8f8;
	}
	.user-header{
		width: 750rpx;
		height: 70vw;
		background: rgb(250,67,106);
		background-image: url("/static/images/user/user-bg.png");
		background-position: 0% 0%;
		background-size: 100% 100%;
		background-repeat: no-repeat;
		position: relative;
		.user-info{
			position: absolute;
			top: 70rpx;
			left: 30rpx;
			width: 320rpx;
			height: 130rpx;
			align-items: center;
			text{
				font-size: 36rpx;
				color: #fff;
			}
		}
		.avatar{
			width: 130rpx;
			height: 130rpx;
			border: 4rpx solid #fff;
			border-radius: 50%;
			overflow: hidden;
			margin-right: 20rpx;
			image{
				width: 100%;
				height: 100%;
			}
		}
		.card{
			width: 690rpx;
			height: 240rpx;
			position: absolute;
			top: 232rpx;
			left: 30rpx;
			border-radius: 16rpx;
			overflow: hidden;
			background-image: url("/static/images/user/vip-card.png");
			background-position: 0% 0%;
			background-size: 100% 100%;
			background-repeat: no-repeat;
			box-sizing: border-box;
			padding: 30rpx;
			.vip-text{
				color: #f6e5a3;
				font-size: 24rpx;
				line-height: 30rpx;
				display: block;
				margin-left: 20rpx;
			}
			.banquan{
				color: #f6e5a3;
				font-size: 24rpx;
				line-height: 30rpx;
				display: block;
				margin-top: 40rpx;
			}
			.custom-style {
					display: inline-block;
					color: #000;
					background: #f6e5a3;
					width: 140rpx;
					height: 38rpx;
					line-height: 38rpx;
				}
		}
	}
	.all-order{
		height: 300rpx;
		background-color: #fff;
		.all-order-top{
			box-sizing: border-box;
			border-bottom: 1rpx solid #eee;
			padding: 20rpx 40rpx;
			line-height: 60rpx;
			image{
				width: 40rpx;
				height: 40rpx;
			}
			.order-icon{
				font-size: 38rpx;
				color: rgb(250, 67, 106);
				margin-right: 10rpx;
			}
			.all-order-text{
				font-size: 28rpx;
				color: #303133;
			}
		}
	}
</style>
