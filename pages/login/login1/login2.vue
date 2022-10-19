<template>
	<view class="login-container">
		<view class="x-content">
			<view class="login-text">
				<view class="tit">
					欢迎使用
					<text>叮咚顺风车</text>
				</view>
				<view class="desc">共享出行，绿色环保</view>
			</view>
		</view>
		<image class="login-img" src="https://webwlx.oss-cn-beijing.aliyuncs.com/uni-page-template/image/sfc.jpg" mode="widthFix"></image>
		<view class="btn-box x-content">
			<button class="x-flex-alc x-flex-cen">
				<text class="ri-wechat-fill x-icon"></text>
				<text>微信用户一键登录</text>
			</button>

			<view>手机号登录</view>
		</view>
	</view>
</template>

<script></script>

<style lang="scss" scoped>
.login-container {
	.x-content {
		width: 630rpx;
	}
	.login-text {
		margin: 100rpx auto 50rpx auto;
		.tit {
			font-size: 50rpx;
			color: #292c38;
			margin-bottom: 10rpx;
			text {
				font-weight: bold;
				margin-left: 10rpx;
			}
		}
		.desc {
			color: #54596d;
		}
	}
	.login-img {
		width: 100%;
		height: auto;
	}
	.btn-box {
		margin-top: 80rpx;
		text-align: center;
		> view {
			font-size: 28rpx;
			color: #292c38;
		}
		button {
			height: 80rpx;
			border-radius: 10rpx;
			color: #fff;
			font-size: 28rpx;
			background-image: linear-gradient(to right, #f78ca0 0%, #f9748f 19%, #fd868c 60%, #fe9a8b 100%);
			width: 90%;
			margin: 20rpx auto 20rpx auto;
			&::after {
				border: none;
				height: 0;
			}
			.x-icon {
				font-size: 40rpx;
				margin-right: 20rpx;
			}
		}
	}
}
</style>
