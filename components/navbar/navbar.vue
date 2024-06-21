<template>
	<view class="top_head">
		<view
			:style="{
				height: getPlaceholder,
			}"
		></view>
		<view class="header">
			<view class="status-bar" :style="{ height: `${ statusBarHeight }px` }"></view>
			<view class="flex-box align-center" :style="{ height: `${ barHeight }px` }">
				<view v-if="autoBack" class="navBack pl10" @click="$navigateBack()">
					<u-icon name="arrow-left" size="20" color="#333333"></u-icon>
				</view>
				<view v-if="defGaBol" class="home">{{ title }}</view>
				<view v-else :class="[ autoBack ? 'pl20' : 'pl46', 'home']">{{ title }}</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		name: 'navbar',
		props: {
			// 标题
			title: {
				type: String,
				default: 'gtUI'
			},
			// 返回上一级按钮
			autoBack: {
				type: Boolean,
				default: false
			},
			// 适老化大标题
			defGaBol:{
				type: Boolean,
				default: false
			}
		},
		data() {
			return {
				statusBarHeight: 0,
				barHeight: 44
			}
		},
		computed: {
			getPlaceholder() {
				return this.sys().statusBarHeight + 44 + 'px'
			}
		},
		async created() {
			console.log('状态栏高度：：',this.sys().statusBarHeight)
			this.statusBarHeight = this.sys().statusBarHeight
		},
		methods: {
			sys() {
				return uni.getSystemInfoSync()
			}
		}
	}
</script>
<style lang="scss">
	.header {
		position: fixed;
		top: 0;
		z-index: 9999999999999;
		width: 100%;
		// background: linear-gradient(#C9DFFF 0%, #F7F8FA 100%);
		background: linear-gradient(180deg, #C9DFFF 0%, #F7F8FA 100%), #F7F8FA;
		.home {
			color: #333333;
			font-size: 38rpx;
			font-weight: 600;
			white-space: nowrap;
			overflow: hidden;
			text-overflow: ellipsis;
			max-width: 600rpx;
		}
	}
</style>