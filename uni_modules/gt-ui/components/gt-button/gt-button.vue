<template>
	<view 
		class="gt-button"
		:class="[ 
			plain ? `gt-button--plain` : '',
			hairline ? `gt-button--hairline` : '',
			disabled ? `gt-button--disabled` : '',
			square ? `gt-button--square` : '',
			round ? `gt-button--round` : '',
			size ? `gt-button--${size}` : '',
			block ? `gt-button--block` : '',
			`gt-button--${ type }`,
		]"
		:style="setStyle"
	>
		<view v-if="icon" style="width: 48rpx;">
			<gtIcon :name="icon" :color="iconColor"/>
		</view>
		<slot></slot>
		<view v-if="loading">
			<gtLoading v-if="!loadingType" :id="1" :loadingText="loadingText" />
			<gtLoading v-else :id="4" :loadingText="loadingText" />
		</view>
	</view>
</template>

<script lang="ts" setup>
	import gtLoading from '../gt-loading/gt-loading.vue';
	import gtIcon from '../gt-icon/gt-icon.vue';
	import { computed } from 'vue';
	
	const props = defineProps({
		// 按钮类型，可选值为 default primary success warning danger
		type: {
			type: String,
			default: 'defalut'
		},
		// 按钮尺寸，可选值为 normal large small mini
		size: {
			type: String,
			default: 'normal'
		},
		// 是否为朴素按钮 
		plain: {
			type: Boolean,
			default: false
		},
		// 是否使用 0.5px 边框
		hairline: {
			type: Boolean,
			default: false
		},
		// disabled	是否禁用按钮
		disabled: {
			type: Boolean,
			default: false
		},
		// round	是否为圆形按钮
		round: {
			type: Boolean,
			default: false
		},
		// square	是否为方形按钮
		square: {
			type: Boolean,
			default: false
		},
		// 是否是加载状态
		loading: {
			type: Boolean,
			default: false
		},
		// 加载状态类型
		loadingType: {
			type: String,
			default: ''
		},
		// 加载文案
		loadingText: {
			type: String,
			default: ''
		},
		// 自定义icon
		icon: {
			type: String,
			default: ''
		},
		// 自定义icon颜色
		iconColor: {
			type: String,
			default: '#fff'
		},
		// 是否是块级元素
		block: {
			type: Boolean,
			default: false
		},
		// 自定义颜色
		color: {
			type: String,
			default: ''
		}
	})

	// const colors = {
	// 	primary: '#1989fa',
	// 	success: '#07c160',
	// 	danger: '#ee0a24',
	// 	warning: '#ff976a',
	// 	default: '#323233'
	// }
	
	const setStyle = computed(() => {
		if (props.plain && props.color) {
			return {
				border: `2rpx solid ${props.color}`,
				color: `${props.color}`,
				background: '#fff'
			}
		}
		
		if (props.color) {
			return {
				color: '#fff',
				background: `${props.color}`
			}
		}
	})
	
</script>
<style lang="scss" scoped>
	@import './gt-button.scss';
	.main {
		color: $gt-primary-color;
	}
</style>