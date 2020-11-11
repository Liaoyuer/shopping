<template>
	<view class="recommend">
		<!-- 宫格布局 -->
		<view v-if="pailie=='gongge'" class="recommend flex justify-between flex-wrap" style="background: #F8F8F8;overflow: hidden;">
			<view class="box" v-for="(item,index) in dataList" :key="item.goods_id">
				<view class="top">
					<image :src="item.img" mode=""></image>
					<image class="tags" v-if="item.baoyou" :src="tagImg[0]"></image>
				</view>
				<view class="bottom-text">
					{{item.title}}
				</view>
				<view class="price">
					<text class="new-price">￥ {{item.money}}</text>
					<text class="old-price">￥ {{item.hmoney}}</text>
				</view>
				<view class="goumai flex justify-between">
					<view class="text flex">
						<text class="text-1" v-if="item.youhui">优惠券</text>
						<text class="text-2" v-if="item.baoyou">包邮</text>
					</view>
					<view class="cart">
						<image src="../static/images/tabBar/cart-default.png" mode=""></image>
					</view>
				</view>
			</view>
		</view>
		<!-- 列表布局 -->
		<view v-if="pailie=='liebiao'" class="list flex justify-between" v-for="(item,index) in goodsList" :key="item.goods_id">
			<image :src="item.img" mode=""></image>
			<view class="list-right flex flex-direction">
				<view class="title">
					{{item.title}}
				</view>
				<view class="flex flex-direction">
					<view class="flex">
						<view class="youhui" v-if="item.youhui">
							优惠券
						</view>
						<view class="youhui" v-if="item.baoyou">
							包邮
						</view>
					</view>
					<view class="youhui-bottom">
						<view class="flex justify-between">
							<view>
								<text class="new-price">￥{{item.money}}</text>
								<text class="old-price">￥{{item.hmoney}}</text>
							</view>
							<image src="../static/images/tabBar/cart-rad.png" mode=""></image>
						</view>
					</view>
				</view>
			</view>
		</view>
		<view class="bottom">
			—— 到底啦 ——
		</view>
	</view>
</template>

<script>
	export default{
		props:{dataList: {type: Array},pailie:{type: String},goodsList:{type: Array}},
		data(){
			return{
				tagImg:[
					'/static/images/home/five.png',
				]
			}
		}
	}
</script>

<style lang="scss">
	.recommend{
		width: 100%;
		.bottom{
			width: 100%;
			text-align: center;
			color: #ccc;
		}
		.box{
			width: 48%;
			height: 530rpx;
			border-radius: 16rpx;
			background-color: #fff;
			margin-bottom: 20rpx;
			.top{
				position: relative;
				height: 60%;
				border-radius: 16rpx;
				image{
					width: 100%;
					height: 100%;
					border-radius: 16rpx;
					display: block;
				}
				.tags{
					position: absolute;
					width: 25%;
					height: 25%;
					top: 0;
					left: 0;
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
				color: #000;
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
						width: 100rpx;
						height: 38rpx;
						line-height: 38rpx;
						box-sizing: border-box;
						// padding: 4rpx;
						border-radius: 12rpx;
						color: #fa436a;
						background-color: #FAEFF7;
					}
					.text-1{
						margin-right: 10rpx;
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
	.list{
		width: 100%;
		height: 190rpx;
		box-sizing: border-box;
		padding: 10rpx;
		position: relative;
		&::before{
			content: "";
			width: 96%;
			height: 2rpx;
			background: #eee;
			position: absolute;
			bottom: 0;
		}
		image{
			width: 126rpx;
			height: 126rpx;
			overflow: hidden;
			border-radius: 10rpx;
		}
		.list-right{
			width: 392rpx;
			.title{
				font-size: 28rpx;
				font-weight: bold;
				color: #333;
				height: 76rpx;
				line-height: 38rpx;
				overflow: hidden;
			}
			.youhui{
				width: 92rpx;
				background: #FAEFF7;
				color: #fa436a;
				font-size: 22rpx;
				text-align: center;
				border-radius: 8rpx;
				margin: 8rpx 0;
				margin-right: 10rpx;
			}
			.youhui-bottom{
				height: 26rpx;
				.new-price{
					font-size: 30rpx;
					font-weight: 600;
					color: #fa436a;
					margin-right: 30rpx;
				}
				.old-price{
					text-decoration: line-through;
					font-size: 22rpx;
					color: #999;
				}
				image{
					width: 36rpx;
					height: 32rpx;
				}
			}
		}
	}
	
</style>
