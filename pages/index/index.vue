<template>
	<view>
		<view class="demo-home">
			<view class="demo-home__title">
				<image src="http://cdn.xuanyunet.com/common%2Fimages%2Flogo.svg" mode="widthFix"></image>
				<text>xuanyu ui uniapp</text>
			</view>
			<view class="demo-home__desc">基于 Vant 轻量、可靠的 UniApp 组件库</view>
			<view class="demo-home-nav" v-for="(item, index) in list" :key="index">
				<view class="demo-home-nav__title">{{ item.title }}</view>
				<view class="demo-home-nav__group">
					<navigator v-for="(nav, navIndex) in item.children" :key="navIndex" :url="nav.url" class="demo-home-nav__block">{{ nav.name }}</navigator>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
export default {
	data() {
		return {
			list: [
				{
					title: '基础组件',
					children: [
						{
							name: 'Button 按钮',
							url: '/element/button/button'
						},
						{
							name: 'Cell 单元格',
							url: '/element/cell/cell'
						},
						{
							name: 'Image 图片',
							url: '/element/image/image'
						},
						{
							name: 'Layout 布局',
							url: '/element/col/col'
						},
						{
							name: 'Popup 弹出层',
							url: '/element/popup/popup'
						}
					]
				},
				{
					title: '表单组件',
					children: [
						{
							name: 'Checkbox 复选框',
							url: '/element/checkbox/checkbox'
						},
						{
							name: 'Field 输入框',
							url: '/element/field/field'
						},
						{
							name: 'Radio 单选框',
							url: '/element/radio/radio'
						},
						{
							name: 'Rate 评分',
							url: '/element/rate/rate'
						},
						{
							name: 'Search 搜索',
							url: '/element/search/search'
						},
						{
							name: 'Slider 滑块',
							url: '/element/slider/slider'
						},
						{
							name: 'Stepper 步进器',
							url: '/element/stepper/stepper'
						},
						{
							name: 'Switch 开关',
							url: '/element/switch/switch'
						},
						{
							name: 'Uploader 文件上传',
							url: '/element/uploader/uploader'
						}
					]
				},
				{
					title: '反馈组件',
					children: [
						{
							name: 'ActionSheet 上拉菜单',
							url: '/element/action-sheet/action-sheet'
						},
						{
							name: 'Dialog 弹出框',
							url: '/element/dialog/dialog'
						},
						{
							name: 'Loading 加载',
							url: '/element/loading/loading'
						}
					]
				},
				{
					title: '展示组件',
					children: [
						{
							name: 'divider 分割线',
							url: '/element/divider/divider'
						},
						{
							name: 'NoticeBar 通知栏',
							url: '/element/notice-bar/notice-bar'
						},
						{
							name: 'Panel 面板',
							url: '/element/panel/panel'
						},
						{
							name: 'Steps 步骤条',
							url: '/element/steps/steps'
						},
						{
							name: 'Tag 标记',
							url: '/element/tag/tag'
						}
					]
				},
				{
					title: '导航组件',
					children: [
						{
							name: 'Grid 宫格',
							url: '/element/grid/grid'
						},
						{
							name: 'NavBar 导航栏',
							url: '/element/nav-bar/nav-bar'
						},
						{
							name: 'Sidebar 侧边导航',
							url: '/element/sidebar/sidebar'
						},
						{
							name: 'Tab 标签页',
							url: '/element/tab/tab'
						},
						{
							name: 'Tabbar 标签栏',
							url: '/element/tabbar/tabbar'
						},
						{
							name: 'TreeSelect 分类选择',
							url: '/element/tree-select/tree-select'
						}
					]
				},
				{
					title: '业务组件',
					children: [
						{
							name: 'AddressEdit 地址编辑',
							url: '/element/address-edit/address-edit'
						},
						{
							name: 'Card 商品卡片',
							url: '/element/card/card'
						},
						{
							name: 'Contcat 联系人',
							url: '/element/contact-card/contact-card'
						},
						{
							name: 'Comment 评论',
							url: '/element/comment/comment'
						},
						{
							name: 'GoodsAction 商品导航',
							url: '/element/goods-action/goods-action'
						},
						{
							name: 'SubmitBar 提交订单栏',
							url: '/element/submit-bar/submit-bar'
						},
						{
							name: 'Sku 商品规格',
							url: '/element/sku/sku'
						}
					]
				}
			]
		};
	},
	onShareAppMessage() {}
};
</script>

<style lang="scss" scoped>
.demo-home {
	box-sizing: border-box;
	width: 100%;
	min-height: 100vh;
	padding: 46px 20px 20px;
	background: #fff;
	&__title {
		margin: 0 0 16px;
		font-size: 32px;
		display: flex;
		align-items: center;
		image {
			width: 40px;
		}
		text {
			margin-left: 16px;
		}
	}
	&__desc {
		margin: 0 0 40px;
		color: rgba(69, 90, 100, 0.6);
		font-size: 14px;
	}
	&-nav {
		&__title {
			margin: 24px 0 8px 16px;
			color: rgba(69, 90, 100, 0.6);
			font-size: 14px;
		}
		&__block {
			position: relative;
			display: -webkit-box;
			display: -webkit-flex;
			display: flex;
			margin: 0 0 12px;
			padding-left: 20px;
			color: #323233;
			font-weight: 500;
			font-size: 14px;
			line-height: 40px;
			background: #f7f8fa;
			border-radius: 99px;
			-webkit-transition: background 0.3s;
			transition: background 0.3s;
		}
	}
}
</style>
