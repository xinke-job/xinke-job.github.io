<template>
	<view class="page" :style="{backgroundImage: 'url(' + imgInfo.bgImg + ')'}">
		<view class="title-box">
			<image class="title" :src="imgInfo.titleImg" />
			<image class="icon" :src="imgInfo.titleIcon" :style="{'width': iconWidth + 'rpx','height': iconHeight + 'rpx'}"/>
		</view>
		<view class="video-box">
			<image class="title" :src="imgInfo.contTitle" />
			<view class="video-cont">
				<image :src="imgInfo.borderImg" />
				<view class="video-cont-cont">
					<video class="video" id="myVideo" :src="imgInfo.videoUrl" @error="videoErrorCallback" controls :poster="imgInfo.videoImg"></video>
				</view>
			</view>
		</view>
		<view class="cont">
			<image :src="imgInfo.contImg" />
		</view>
		<view class="btn" @click="goPath">
			<image src="../../static/image/btn.png" />
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return{
				imgInfo: {
					bgImg: '',
					titleImg: '',
					titleIcon: '',
					contTitle: '',
					borderImg: '',
					contImg: ''
				},
				iconWidth: '',
				iconHeight: ''
			}
		},
		onLoad(options) {
			console.log('options', options.type)
			switch (options.type){
				case '1':
					this.imgInfo ={
						bgImg: '../../static/image/car-bg.png',
						titleImg: '../../static/image/car-title.png',
						titleIcon: '../../static/image/car-icon.png',
						contTitle: '../../static/image/car-tit.png',
						borderImg: '../../static/image/car-border.png',
						contImg: '../../static/image/car-cont.png',
						videoImg: '../../static/image/list1-vimg.png',
						videoUrl: '../../static/video/list1.mp4'
					}
					this.iconWidth = '464',
					this.iconHeight = '272'
					break;
				case '2':
					this.imgInfo ={
						bgImg: '../../static/image/list2-bg.png',
						titleImg: '../../static/image/list2-title.png',
						titleIcon: '../../static/image/list2-icon.png',
						contTitle: '../../static/image/list2-tit.png',
						borderImg: '../../static/image/list2-border.png',
						contImg: '../../static/image/list2-cont.png',
						videoImg: '../../static/image/list2-vimg.png',
						videoUrl: '../../static/video/list2.mp4'
					}
					this.iconWidth = '466',
					this.iconHeight = '296'
					break;
				case '3':
					this.imgInfo ={
						bgImg: '../../static/image/list3-bg.png',
						titleImg: '../../static/image/list3-title.png',
						titleIcon: '../../static/image/list3-icon.png',
						contTitle: '../../static/image/list3-tit.png',
						borderImg: '../../static/image/list3-border.png',
						contImg: '../../static/image/list3-cont.png',
						videoImg: '../../static/image/list3-vimg.png',
						videoUrl: '../../static/video/list3.mp4'
					}
					this.iconWidth = '403',
					this.iconHeight = '284'
					break;
				default:
					this.imgInfo ={
						bgImg: '../../static/image/list4-bg.png',
						titleImg: '../../static/image/list4-title.png',
						titleIcon: '../../static/image/list4-icon.png',
						contTitle: '../../static/image/list4-tit.png',
						borderImg: '../../static/image/list4-border.png',
						contImg: '../../static/image/list4-cont.png',
						videoImg: '../../static/image/list4-vimg.png',
						videoUrl: '../../static/video/list4.mp4'
					}
					this.iconWidth = '373',
					this.iconHeight = '302'
					break;
			}
		},
		methods: {
			goPath() {
				uni.navigateTo({
					url: '/pages/home/get'
				});
			}
		},
	}
</script>

<style lang="scss" scoped>
	.page{
		background-position: top left;
		background-size: cover;
		width: 100%;
		min-height: 100vh;
		display: flex;
		flex-direction: column;
		align-items:center;
		.title-box{
			padding-top:43rpx;
			position: relative;
			text-align: center;
			.title{
				width: 471rpx;
				height: 172rpx;
			}
			.icon{
				width: 464rpx;
				height: 273rpx;
				margin-left:120rpx;
			}
		}
		.video-box{
			text-align: center;
			.title{
				width: 402rpx;
				height: 72rpx;
			}
			.video-cont{
				position:relative;
				margin-top: -12rpx;
				image{
					width: 682rpx;
					height: 390rpx;
				}
				&-cont{
					position: absolute;
					top: 18rpx;
					left: 18rpx;
					.video{
						width: 650rpx;
						height: 354rpx
					}
				}
			}
		}
		.cont{
			margin-top:51rpx;
			text-align: center;
			image{
				width: 680rpx;
				height: 809rpx;
			}
		}
		.btn{
			padding:50rpx 0;
			image{
				width: 407rpx;
				height: 89rpx;
			}
		}
	}
</style>