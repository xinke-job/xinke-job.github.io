<template>
	<view class="page">
		<image src="../../static/image/get-title.png" />
		<image  class="msg" src="../../static/image/get-text.png" />
		<image class="icon" src="../../static/image/get-icon.png" />
		<image src="../../static/image/get-qrcode.png" />
	</view>
</template>

<script>
</script>

<style lang="scss" scoped>
	.page{
		background-image: url("../../static/image/get-bg.jpg");
		background-position: top left;
		background-size: cover;
		width: 100%;
		min-height: 100vh;
		display: flex;
		flex-direction: column;
		align-items:center;
		image{
			&:first-child{
				width: 610rpx;
				height: 192rpx;
				margin-top: 100rpx;
			}
			&:last-child{
				width: 663rpx;
				height:540rpx;
				margin-top: -100rpx;
				z-index: 99;
			}
		}
		.msg{
			height: 64rpx;
			width: 478rpx;
			margin-top:35rpx;
		}
		.icon{
			width: 368rpx;
			height: 456rpx;
			margin-top: 24rpx;
			z-index:9;
		}
	}
</style>