<template>
	<view>
		<text 
			class="gt-icons"
			:class="[`gtui-${name}`, loading ? 'spinner' : '' ]"
			:style="{ 
				fontSize: setIconSize, 
				color: color
			}"
		></text>
	</view>
</template>

<script lang="ts" setup>
	import { computed } from 'vue';
	const props = defineProps({
		name: {
			type: String,
			default: '-'
		},
		// 默认size是20px
		size: {
			type: [ String || Number ],
			default: 20
		},
		color: {
			type: String,
			default: 'inherit'
		},
		loading: {
			type: Boolean,
			default: false
		}
	})
	// 默认使用px，也可以带有rpx
	const setIconSize = computed(() => {
		return typeof props.size === 'string' && props.size.includes('px') ? props.size : `${props.size}px`
	})
</script>

<style lang="scss" scoped>

	/* #ifndef APP-NVUE */
	@import './gticons.css';
	
	@font-face {
		font-family: gticons;
		src: url('./gticons.ttf');
	}
	
	/* #endif */
	.gt-icons {
		font-family: gticons;
		text-decoration: none;
		text-align: center;
	}
	
	.spinner {
		display: inline-block;
	  height: 35px;
	  width: 35px;
	  animation: rotate 1s ease-in-out infinite;
	}
	@keyframes rotate {
	  0%   { transform: rotate(0);      }
	  to { transform: rotate(1turn); }
	}
	
</style>