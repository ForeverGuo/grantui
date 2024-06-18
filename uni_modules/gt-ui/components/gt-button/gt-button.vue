<template>
	<view 
		class="gt-button"
		:class="[ 
			plain ? `gt-button--plain` : '',
			hairline ? `gt-button--hairline` : '',
			disabled ? `gt-button--disabled` : '',
			square ? `gt-button--square` : '',
			round ? `gt-button--round` : '',
			`gt-button--${ type }`,
		]"
	>
		<slot></slot>
	</view>
</template>

<script lang="ts" setup>
	defineProps({
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
		}
	})
</script>
<style lang="scss" scoped>
	@import './gt-button.scss';
	.main {
		color: $gt-primary-color;
	}
</style>