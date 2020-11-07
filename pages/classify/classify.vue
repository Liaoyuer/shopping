<template>
	<view class="classify">
		<view class="head width-90 flex justify-between">
			<search class="search"></search>
			<u-icon name="grid" size="52" color="#fa5376"></u-icon>
		</view>
		<view class="bottom flex justify-between">
			<view class="menu">
				<view class="menu-item" v-for="(item,index) in categoryList" :key="index" :class="isActive==index?'menu-item-active':''" @click="selectMenu(index)">
					{{item.name}}
				</view>
			</view>
			<view class="goodsList">
				<view class="goodsList-top flex justify-end">
					<text>销量</text>
					<view class="iconup flex-wrap">
						<u-icon name="arrow-up-fill" color="#999999" size="14"></u-icon>
						<u-icon name="arrow-down-fill" color="#999999" size="14"></u-icon>
					</view>
					<text>价格</text>
					<view class="iconup flex-wrap">
						<u-icon name="arrow-up-fill" color="#999999" size="14"></u-icon>
						<u-icon name="arrow-down-fill" color="#999999" size="14"></u-icon>
					</view>
				</view>
				<view class="goodsList-bottom">
					
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	import search from '../../components/search.vue'
	export default {
		data() {
			return {
				isActive: 0,
				categoryList: [{ //分类列表
					id: 1,
					name: '饼干',
				
				}, {
					id: 2,
					name: '布丁',
				
				}, {
					id: 3,
					name: '甜甜圈',
				
				}, {
					id: 4,
					name: '面包',
				
				}, {
					id: 5,
					name: '薯片',
				
				}, {
					id: 6,
					name: '热狗',
				
				}, {
					id: 7,
					name: '冰淇淋',
				
				}, {
					id: 8,
					name: '奶油草莓',
				
				}, {
					id: 9,
					name: '披萨',
				
				}, {
					id: 10,
					name: '蛋黄酥',
				
				}
				],
			}
		},
		methods: {
			selectMenu(index){
				this.isActive = index
			}
		},
		components:{
			search
		}
	}
</script>

<style lang="scss">
	.classify{
		height: 100%;
		.head{
			height: 100rpx;
			line-height: 100rpx;
			.search{
				width: 90%;
			}
		}
		.bottom{
			width: 750rpx;
			height: 100%;
			background: pink;
			.menu{
				width: 26%;
				height: 100%;
				background: #f8f8f8;
				.menu-item{
					width: 100%;
					height: 80rpx;
					line-height: 80rpx;
					text-align: center;
				}
			}
			.goodsList{
				width: 73%;
				height: 100%;
				background: #f8f8f8;
				.goodsList-top{
					width: 100%;
					height: 70rpx;
					line-height: 70rpx;
					color: #999999;
					font-size: 26rpx;
				}
				.goodsList-bottom{
					width: 100%;
					height: 100%;
					background: #fff;
				}
			}
		}
	}
	.menu-item-active{
		width: 100%;
		height: 80rpx;
		line-height: 80rpx;
		text-align: center;
		background: #fff;
		color: #fa5376;
		border-left: 6rpx solid #fa5376;
		box-sizing: border-box;
	}
</style>
