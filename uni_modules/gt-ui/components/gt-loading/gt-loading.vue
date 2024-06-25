<template>
	<view class="gt-loading">
		<image v-if="id === 1" class="spinner" src="./icons/loading1.svg"></image>
		<image v-if="id === 2" class="spinner" src="./icons/loading2.svg"></image>
		<image v-if="id === 3" class="spinner" src="./icons/loading3.svg"></image>
		<image v-if="id === 4" class="spinner" src="./icons/loading4.svg"></image>
		<text v-if="loadingText" class="loading-text">{{ loadingText }}</text>
	</view>
</template>

<script lang="ts" setup>
	defineProps({
		id: {
			type: Number,
			default: 1
		},
		loadingText: {
			type: String,
			default: ''
		}
	})
</script>

<style lang="scss" scoped>
	.gt-loading {
		background: transparent;
		display: flex;
		align-items: center;
		justify-content: center;
		.loading-text {
			color: #fff;
			font-size: 28rpx;
			margin-left: 10rpx;
		}
	}
	.spinner {
	  height: 30px;
	  width: 30px;
	  animation: rotate 1s ease-in-out infinite;
	}
	@keyframes rotate {
	  0%   { transform: rotate(0);      }
	  to { transform: rotate(1turn); }
	}
</style>
