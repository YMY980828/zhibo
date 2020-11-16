<template>
	<view class="content">
		<!-- 轮播图 s -->
		<swiper indicator-active-color="#8745FF" :indicator-dots="true" :autoplay="true" :circular="true" indicator-color="rgba(255,255,255,1)">
			<swiper-item>
				<image style="width: 100%;" src="../../common/images/banner1.jpg" mode="widthFix"></image>
			</swiper-item>
			<swiper-item>
				<image style="width: 100%;" src="../../common/images/banner2.jpg" mode="widthFix"></image>
			</swiper-item>
			<swiper-item>
				<image style="width: 100%;" src="../../common/images/banner3.jpg" mode="widthFix"></image>
			</swiper-item>
			<swiper-item>
				<image style="width: 100%;" src="../../common/images/banner4.jpg" mode="widthFix"></image>
			</swiper-item>
		</swiper>
		<!-- 轮播图 e -->
		<!-- 直播列表 s -->
		<view class="list-wrapper">
			<view @click="openLive" class="odd" >
				<view style="width: 100%;" class="">
					<image style="width: 100%;height: 375rpx;" src="../../common/images/1.jpg" mode="aspectFill"></image>
				</view>
			</view>
			<view class="evel">
				<view style="width: 100%;" class="">
					<image style="width: 100%;height: 375rpx;" src="../../common/images/tool2.jpeg" mode="aspectFill"></image>
				</view>
			</view>
			<view class="odd">
				<view style="width: 100%;" class="">
					<image style="width: 100%;height: 375rpx;" src="../../common/images/tool3.jpeg" mode="aspectFill"></image>
				</view>
			</view>
		</view>
		<!--直播列表 e -->
		
		
	</view> 
</template>

<script>
	export default {
		data() {
			return {
				title: '我爱于明仪!'
			}
		},
		onLoad() {

		},  
		methods: {
			openLive(){
				uni.navigateTo({
					url:"../live/live"
				})
			}
		}
	}
</script>

<style lang="less">
	.list-wrapper{
		display: flex;  
		flex-wrap:wrap ;
		&>view{
			width: 50%;
			box-sizing: border-box;
			margin-top: 20rpx;
			&>view{
				image{
					vertical-align: bottom;
				}
			}
			
		}
		.odd{
			padding-left: 20rpx;
			padding-right: 10rpx;
		}
		.evel{
			padding-left: 10rpx;
			padding-right: 20rpx;
		}
	}
</style>
