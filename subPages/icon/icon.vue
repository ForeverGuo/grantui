<template>
	<navbar />
	<view class="icon">
		<view class="flex-box flex-wrap ">
			<gt-icon class="icon-item" v-for="(item, index) in iconArray" :key="index" :name="item" size="30" />
		</view>
	</view>
</template>

<script lang="ts" setup>
	import { reactive } from 'vue';
	const iconArray = reactive([
		'woman',
		'man',
		'adduser',
		'deleteuser',
		'addteam',
		'deleteteam',
		'user',
		'team',
		'left',
		'right',
		'up',
		'down',
		'arrowleft',
		'arrowright',
		'arrowup',
		'arrowdown',
		'like',
		'unlike',
		'fullscreen',
		'fullscreen-exit',
		'image',
		'check-circle',
		'close-circle',
		'setting',
		'setting-fill',
		'phone',
		'phone-fill',
		'home',
		'home-fill',
		'caret-down',
		'caret-up',
		'caret-left',
		'caret-right',
		'xing',
		'xing-fill',
		'saoma',
		'shanchu',
		'shenfen',
		'sousuo',
		'tongzhi',
		'tongzhi-fill',
		'tuikuan',
		'wuliu',
		'xihuan',
		'xihuan-fill',
		'xinxi',
		'xinxi-fill',
		'zuobiao',
		'zuobiao-fill',
		'erweima',
		'alipay',
		'weibo',
		'alipay-circle-fill',
		'wechat-fill',
		'QQ-circle-fill'
	])
</script>

<style lang="scss" scoped>
	.icon {
		padding: 30rpx;
		.icon-item {
			padding: 10rpx;
			border: 2rpx solid #efefef;
			margin: 0 22rpx 25rpx 0;
			border-radius: 10rpx;
			width: 10%;
			text-align: center;
		}
	}
</style>