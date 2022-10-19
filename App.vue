<script>
export default {
	onLaunch: function() {
		uni.loadFontFace({
			family: 'remixicon',
			global: true,
			source: 'https://webwlx.oss-cn-beijing.aliyuncs.com/uni-page-template/font/remixicon.ttf',
			fail(err) {
			console.log('字体包加载失败');
			}
		});
	},
	onShow: function() {},
	onHide: function() {}
};
</script>

<style lang="scss">
/*每个页面公共css */
@import '@/uview-ui/index.scss';
</style>
