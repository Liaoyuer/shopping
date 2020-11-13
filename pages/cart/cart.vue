<template>
	<view class="cart">
		<view class="clear-invalid width-90">
			清空失效商品
		</view>
		<view class="cart-item width-90 flex">
			<u-checkbox @change="checkboxChange" size="30" shape="circle" active-color="#fa5376" class="select-dot"></u-checkbox>
			<view class="flex justify-between" style="width: 100%;">
				<view class="image">
					<image src="../../static/images/face.jpg" mode=""></image>
					<view class="invalid-mask">
						已失效
					</view>
				</view>
				<view class="cart-item-right flex flex-direction">
					<view class="title">
						DUNKINDONUTS唐恩都乐美国甜甜圈6个礼盒装
					</view>
					<view class="attribute">
						<text>草莓味【8枚】</text>
					</view>
					<view class="flex justify-between">
						<text class="price">￥35.90</text>
						<view class="group flex">
							<icon class="iconfont icon-jian2"></icon>
							<input disabled="true" class="input" type="text" value="1" />
							<icon class="iconfont icon-jia"></icon>
						</view>
					</view>
				</view>
			</view>
		</view>
		<view class="cart-item width-90 flex">
			<u-checkbox @change="checkboxChange" size="30" shape="circle" active-color="#fa5376" class="select-dot"></u-checkbox>
			<view class="flex justify-between" style="width: 100%;">
				<view class="image">
					<image src="../../static/images/face.jpg" mode=""></image>
					<view class="invalid-mask">
						已失效
					</view>
				</view>
				<view class="cart-item-right flex flex-direction">
					<view class="title">
						DUNKINDONUTS唐恩都乐美国甜甜圈6个礼盒装
					</view>
					<view class="attribute">
						<text>草莓味【8枚】</text>
					</view>
					<view class="flex justify-between">
						<text class="price">￥35.90</text>
						<view class="group flex">
							<icon class="iconfont icon-jian2"></icon>
							<input disabled="true" class="input" type="text" value="1" />
							<icon class="iconfont icon-jia"></icon>
						</view>
					</view>
				</view>
			</view>
		</view>
		<view class="cart-bottom">
			<view class="flex justify-between width-90">
				<view class="cart-bottom-left">
					<u-checkbox @change="checkboxChange" size="30" shape="circle" active-color="#fa5376" class="select-dot">全选</u-checkbox>
				</view>
				<view class="cart-bottom-right flex justify-between">
					<text>合计：￥0</text>
					<u-button class="custom-style" shape="circle" :hair-line="false" size="mini">结算(0)</u-button>
					<!-- <button type="circle">结算</button> -->
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		methods: {
			checkboxChange(e) {
						console.log(e);
					},
		}
	}
</script>

<style lang="scss">
	.cart{
		height: 100%;
		.clear-invalid{
			color: rgb(250, 67, 106);
			text-align: right;
			padding: 20rpx 0;
		}
		.cart-item{
			box-shadow: #eee 0 2rpx 6rpx 5rpx;
			border-radius: 8rpx;
			height: 200rpx;
			margin-bottom: 20rpx;
			.select-dot{
				margin-left: 20rpx;
			}
			.image{
				width: 165rpx;
				height: 165rpx;
				margin: 10rpx;
				position: relative;
				image{
					width: 100%;
					height: 100%;
					
				}
				.invalid-mask{
					position: absolute;
					top: 0;
					left: 0;
					width: 100%;
					height: 100%;
					line-height: 165rpx;
					color: #fff;
					font-size: 24rpx;
					text-align: center;
					background: rgba(0,0,0,0.5);
				}
			}
			.cart-item-right{
				width: 460rpx;
				box-sizing: border-box;
				padding: 10rpx;
				.title{
					width: 100%;
					height: 68rpx;
					line-height: 34rpx;
					overflow: hidden;
					font-size: 24rpx;
					color: #333;
				}
				.attribute{
					padding: 4rpx 0;
					text{
						font-size: 22rpx;
						box-sizing: border-box;
						padding: 5rpx;
						background: #f3f3f3;
						color: #a7a7a7;
						border-radius: 8rpx;
					}
				}
				.price{
					font-size: 15px;
					color: #fa436a;
				}
				.group{
					// font-size: 24rpx;
					.input{
						display: block;
						background-color: #eee;
						width: 50rpx;
						margin: 0 10rpx;
						color: #fa436a;
						text-align: center;
					}
				}
			}
		}
		.cart-bottom{
			position: fixed;
			bottom: 100rpx;
			width: 100%;
			height: 100rpx;
			line-height: 100rpx;
			.cart-bottom-left{
				width: 30%;
			}
			.cart-bottom-right{
				width: 50%;
				align-items: center;
				.custom-style {
						display: inline-block;
						color: #fff;
						background: #fa436a;
					}
			}
		}
	}
</style>
