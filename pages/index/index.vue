<template>
	<view class="x-content">
		<view class="list-container">
			<view class="list-header x-flex">
				<view>页面名称</view>
				<view>操作</view>
			</view>
			<view class="list-item  x-flex-alc" v-for="(item, index) in pages" :key="index">
				<view>{{ getName(item) }}</view>
				<view><u-button class="list-button" text="跳转" type="primary" size="small" @click="goUrl(item)"></u-button></view>
			</view>
		</view>
	</view>
</template>

<script>
import pageData from '@/pages.json';

export default {
	data() {
		return {
			pages: pageData.pages
		};
	},
	onLoad() {},
	methods: {
		getName(item) {
			let name = null;
			let pathArr = item.path.split('/');
			name = item?.style?.navigationBarTitleText ?? pathArr[pathArr.length - 1];
			return name;
		},
		goUrl({path}){
			uni.$u.route({
				url:path
			})
			
		}
	}
};
</script>
<style lang="scss" scoped>
$opt-width: 200rpx;
.list-container {
	margin-top: 40rpx;
	@include x-flex();
	border-left: 1px solid #f7f7f7;
	border-right: 1px solid #f7f7f7;
	flex-direction: column;
	.list-header {
		@include x-flex-btn();
		text-align: left;
		line-height: 100rpx;
		background: #f7f7f7;
		font-size: 28rpx;
		> view {
			padding: 0 20rpx;
		}
		> view:last-child {
			width: $opt-width;
			flex-shrink: 0;
		}
	}
	.list-item {
		@include x-flex-btn();
		line-height: 100rpx;
		border-bottom: 1px solid #f7f7f7;
		font-size: 28rpx;
		> view {
			padding: 0 20rpx;
		}
		> view:last-child {
			width: $opt-width;
			flex-shrink: 0;
		}
		.list-button{
			width: 80rpx;
			margin: 0;
		}
	}
}
</style>
