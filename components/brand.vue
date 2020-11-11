<template>
	<view class="brand">
		<image src="https://img.zcool.cn/community/01e47655efeee832f875a132e43a9c.png@1280w_1l_2o_100sh.png"></image>
		<view class="brand-classify width-90">
			<u-grid :col="3">
				<u-grid-item class="u-grid-item" v-for="(item,index) in classData" :key="index">
					<image :src="item.img" class="category-image"></image>
					<view class="grid-text">{{item.name}}</view>
				</u-grid-item>
			</u-grid>
		</view>
		<view class="bottom">
			—— 到底啦 ——
		</view>
	</view>
</template>

<script>
	export default {
		props:{
			classData:{type: Array}
		},
		data() {
			return {
				
			}
		},
		methods: {
			
		}
	}
</script>

<style lang="scss">
	.brand{
		image{
			width: 100%;
			height: 184rpx;
		}
		.brand-classify{
			.category-image{
				width: 100rpx;
				height: 36rpx;
			}
			.grid-text{
				color: #333;
				font-size: 24rpx;
				font-weight: bold;
				margin-top: 20rpx;
			}
			.u-grid-item{
				padding: 10rpx 0;
			}
		}
		.bottom{
			width: 100%;
			text-align: center;
			color: #ccc;
		}
	}
</style>
