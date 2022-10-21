<template>
	<view class="page">
		<view class="bg">
			<view class="title">
				<image src="../../static/image/title.png"></image>
				<image src="../../static/image/qilin.png"></image>
			</view>
			<view class="list">
				<view class="list-item" v-for="(item,index) in list" :key="index" @click="goPath(item.url)">
					<image :src="item.icon"/>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return{
				list: [
					{icon: '../../static/image/list01.png', url: '/pages/home/carOwner?type=1'},
					{icon: '../../static/image/list02.png', url: '/pages/home/carOwner?type=2'},
					{icon: '../../static/image/list03.png', url: '/pages/home/carOwner?type=3'},
					{icon: '../../static/image/list04.png', url: '/pages/home/carOwner?type=4'},
				]
			}
		},
		methods:{
			goPath(url) {
				console.log('url', url)
				uni.navigateTo({
					url: url
				});
			}
		}
	}
</script>

<style lang="scss" scoped>
	.page{
		min-height: 100vh;
		width: 100%;
		.bg{
			background-image: url("../../static/image/bg.png");
			background-position: top left;
			background-size: cover;
			width: 100%;
			min-height: 100vh;
			display: flex;
			flex-direction: column;
			align-items:center;
			.title{
				margin-top: 57rpx;
				text-align: center;
				image{
					width: 249rpx;
					height: 318rpx;
					&:first-child{
						width:568rpx;
						height:224rpx;
					}
					&:last-child{
						margin-top: -40rpx;
						margin-left: 100rpx;
					}
					
				}
			}
			.list{
				margin-top: 140rpx;
				position:relative;
				width: 100%;
				text-align:center;
				&-item{
					margin-bottom: 32rpx;
					text-align:center;
					image{
						width: 708rpx;
						height: 497rpx;
					}
				}
			}
		}
	}
</style>