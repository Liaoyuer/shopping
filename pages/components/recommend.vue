<template>
	<view class="recommend" style="background: #F8F8F8;overflow: hidden;">
		<view class="box">
			<view class="top">
				<image src="https://img.zcool.cn/community/01e47655efeee832f875a132e43a9c.png@1280w_1l_2o_100sh.png" mode=""></image>
			</view>
			<view class="bottom-text">
				DUNKINDONUTS唐恩都乐美国甜甜圈6个礼盒装 随机搭配6款
			</view>
			<view class="price">
				<text class="new-price">￥ 35.90</text>
				<text class="old-price">￥ 45.90</text>
			</view>
			<view class="goumai flex justify-between">
				<view class="text flex">
					<text class="text-1">优惠券</text>
					<text class="text-2">包邮</text>
				</view>
				<view class="cart">
					<image src="../../static/images/tabBar/cart-default.png" mode=""></image>
				</view>
			</view>
		</view>
		
	</view>
</template>

<script>
	export default{
		props:{dataList: {type: Array}},
		data(){
			return{
				
			}
		}
	}
</script>

<style lang="scss">
	.recommend{
		width: 100%;
		margin-bottom: 500rpx;
		.box{
			width: 48%;
			height: 530rpx;
			border-radius: 16rpx;
			background-color: pink;
			.top{
				height: 60%;
				border-radius: 16rpx;
				image{
					width: 100%;
					height: 100%;
					border-radius: 16rpx;
					display: block;
				}
			}
			.bottom-text{
				box-sizing: border-box;
				padding: 0 10rpx;
				margin-top: 20rpx;
				height: 64rpx;
				line-height: 32rpx;
				overflow: hidden;
				font-size: 24rpx;
				font-weight: block;
			}
			.price{
				margin: 10rpx 0;
				.new-price{
					color: #fa5376;
					font-size: 32rpx;
				}
				.old-price{
					font-size: 22rpx;
					color: #ccc;
					text-decoration: line-through;
					margin-left: 10rpx;
				}
			}
			.goumai{
				box-sizing: border-box;
				padding: 0 10rpx;
				.text{
					.text-1,.text-2{
						display: block;
						text-align: center;
						height: 40rpx;
						line-height: 40rpx;
						box-sizing: border-box;
						padding: 4rpx;
						border-radius: 12rpx;
						color: #fa436a;
						background-color: #FAEFF7;
					}
				}
				.cart{
					width: 40rpx;
					height: 40rpx;
					image{
						width: 100%;
						height: 100%;
					}
				}
			}
		}
		
	}
</style>
