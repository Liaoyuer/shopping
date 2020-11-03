<template>
	<view class="login">
		<image class="logo" src="../../static/images/log.png" mode=""></image>
		<view class="login_from">
			<input class="phone" type="text" placeholder="请输入手机号码" />
			<view class="codes flex justify-between">
				<input class="uni-input" type="idcard" placeholder="请输入验证码" />
				<view>验证码</view>
			</view>
			<u-button class="login_btn" @click="onlogin" shape="circle" :hair-line="false">登录</u-button>
			<view class="login_text">
				—— 快速登录 ——
			</view>
			<image class="wxlogo" src="../../static/images/wx.png" mode=""></image>
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
			onlogin(){
				uni.reLaunch({
					url: "/pages/index/index"
				})
			}
		}
	}
</script>

<style lang="scss">
	.login{
		width: 750rpx;
		height: 100%;
		background: url('https://6d61-matchbox-79a395-1302390714.tcb.qcloud.la/matchbox/img_flower_4.jpg');
		background-size: cover;
		background-repeat:no-repeat;
		background-position: center;
		.logo{
			background: #fff;
			width: 160rpx;
			height: 160rpx;
			border-radius: 50%;
			display: block;
			top: 150rpx;
			margin: 0 auto;
		}
		.login_from{
			// text-align: center;
			width: 80%;
			margin: 0 auto;
			margin-top: 270rpx;
			.phone{
				width: 100%;
				height: 80rpx;
				line-height: 80rpx;
				box-sizing: border-box;
				padding-left: 30rpx;
				border-radius: 10rpx;
				background: #fff;
			}
			.codes{
				width: 100%;
				margin-top: 50rpx;
				input{
					width: 75%;
					height: 80rpx;
					border-radius: 10rpx;
					padding-left: 30rpx;
					line-height: 80rpx;
					background: #fff;
					box-sizing: border-box;
				}
				view{
					width: 20%;
					height: 80rpx;
					line-height: 80rpx;
					text-align: center;
					border-radius: 10rpx;
					color: #fff;
					background: #5f98a1;
				}
			}
		}
		.login_btn{
			width: 80%;
			margin-top: 100rpx;
			color: #fff;
			background: #5f98a1;
		}
		.login_text{
			text-align: center;
			margin: 0 auto;
			margin-top: 150rpx;
			color: #fff;
		}
		.wxlogo{
			width: 100rpx;
			height: 100rpx;
			display: block;
			margin: 0 auto;
		}	
	}
</style>
