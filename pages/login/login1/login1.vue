<template>
	<view class="login-container">
		<view class="status_bar"><!-- 这里是状态栏 --></view>
		<view class="x-content">
			<view class="login-header x-flex-btn x-flex-alc">
				<text class="x-icon ri-arrow-left-line" @click="backBtn"></text>
				<text>遇到问题</text>
			</view>
			<view class="login-logo">
				<view class="logo-box"><image src="https://webwlx.oss-cn-beijing.aliyuncs.com/uni-page-template/image/logo1.svg" mode=""></image></view>
				<view class="logo-text">一款注重用户体验的app</view>
			</view>
			<view class="login-btn-container">
				<button>本机号码一键登录</button>
				<view class="longin-btn-box x-flex-alc">
					<view class="longin-btn-list x-flex-alc">
						<text class="x-icon ri-phone-line"></text>
						<text>手机号登录</text>
					</view>
					<view class="longin-btn-list x-flex-alc">
						<text class="x-icon ri-wechat-2-line"></text>
						<text>微信登录</text>
					</view>
				</view>
			</view>
			<view class="tips-text">
				<text @click="checkFlag = !checkFlag" class="x-icon" :class="checkFlag ? 'ri-checkbox-circle-line' : 'ri-checkbox-blank-circle-line'"></text>
				<text>
					登录即代表您同意
					<text class="link">《用户协议》</text>
					<text class="link">《脆私政策》</text>
					<text class="link">《统一认证服务条款》</text>
				</text>
			</view>
		</view>

		<view class="login-bg"></view>
	</view>
</template>

<script>
export default {
	data() {
		return {
			checkFlag: false
		};
	},
	methods: {
		backBtn() {
			uni.navigateBack();
		}
	}
};
</script>

<style lang="scss" scoped>
.login-container {
	.login-header {
		color: #fff;
		padding: 40rpx 0;
		font-size: 24rpx;
		opacity: 0.6;
		margin-top: var(--status-bar-height);
		/* #ifdef MP-WEIXIN */
		justify-content: flex-start;
		/* #endif */
		.x-icon {
			font-size: 40rpx;
			/* #ifdef MP-WEIXIN */
			margin-right: 20rpx;
			/* #endif */
		}
	}
	.login-logo {
		margin: 300rpx auto 200rpx auto;
		text-align: center;
		.logo-box {
			height: 140rpx;
			width: 140rpx;
			background: #fff;
			border-radius: 20rpx;
			margin: 0 auto 40rpx auto;
			image {
				width: 80%;
				height: 80%;
				margin: 10%;
			}
		}
		.logo-text {
			color: #fff;
			letter-spacing: 10rpx;
			opacity: 0.6;
			font-size: 24rpx;
		}
	}
	.login-btn-container {
		> button {
			width: 600rpx;
			line-height: 90rpx;
			border-radius: 10rpx;
			background: #fff;
			color: #333;
			font-size: 28rpx;
			font-weight: bold;
		}
		.longin-btn-box {
			justify-content: center;
			color: #fff;
			font-size: 28rpx;
			margin-top: 40rpx;
			opacity: 0.7;
			.longin-btn-list {
				.x-icon {
					margin-right: 20rpx;
				}
				&:first-child {
					position: relative;
					padding-right: 40rpx;
					&::after {
						content: '';
						position: absolute;
						width: 1px;
						background: #fff;
						height: 80%;
						right: 0;
						top: 10%;
					}
				}
				&:last-child {
					padding-left: 40rpx;
				}
			}
		}
	}
	.tips-text {
		text-align: center;
		color: rgba(255, 255, 255, 0.7);
		padding: 0 60rpx;
		margin-top: 100rpx;
		line-height: 40rpx;
		font-size: 26rpx;
		.x-icon {
			padding: 10rpx 20rpx 10rpx 0;
			font-size: 36rpx;
			position: relative;
			top: 10rpx;
		}
		.link {
			color: rgba(255, 255, 255, 0.9);
		}
	}
}
.login-bg {
	background-image: url('https://webwlx.oss-cn-beijing.aliyuncs.com/uni-page-template/image/login1.jpg');
	background-position: center center;
	background-size: cover;
	background-repeat: no-repeat;
	position: absolute;
	background-color: rgba(0, 0, 0, 0.8);
	width: 100vw;
	height: 100vh;
	top: 0;
	left: 0;
	z-index: -1;
}
</style>
