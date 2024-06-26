<template>
	<view class="button">
		<view class="mt20 mb30 fs28 c-455a">按钮类型</view>
		<view class="flex-box flex-wrap">
			<gt-button class="mr30 mb20" type="default">默认按钮</gt-button>
			<gt-button class="mr30 mb20" type="primary">信息按钮</gt-button>	
			<gt-button class="mr30 mb20" type="success">主要按钮</gt-button>
			<gt-button class="mr30 mb20" type="danger">危险按钮</gt-button>
			<gt-button class="mr30 mb20" type="warning">警告按钮</gt-button>
		</view>
		
		<view class="mt20 mb30 fs28 c-455a">朴素按钮</view>
		<view class="flex-box flex-wrap">
			<gt-button class="mr30 mb20" plain type="success">朴素按钮</gt-button>
			<gt-button class="mr30 mb20" plain type="primary">朴素按钮</gt-button>	
		</view>
		
		<view class="mt20 mb30 fs28 c-455a">细边框</view>
		<view class="flex-box flex-wrap">
			<gt-button class="mr30 mb20" plain hairline type="success">细边框按钮</gt-button>
			<gt-button class="mr30 mb20" plain hairline type="primary">细边框按钮</gt-button>	
		</view>
		
		<view class="mt20 mb30 fs28 c-455a">禁用状态</view>
		<view class="flex-box flex-wrap">
			<gt-button class="mr30 mb20" disabled type="success">细边框按钮</gt-button>
			<gt-button class="mr30 mb20" disabled type="primary">细边框按钮</gt-button>	
		</view>
		
		<view class="mt20 mb30 fs28 c-455a">按钮形状</view>
		<view class="flex-box flex-wrap">
			<gt-button class="mr30 mb20" square type="success">方形按钮</gt-button>
			<gt-button class="mr30 mb20" round type="primary">圆形按钮</gt-button>	
		</view>
		
		<view class="mt20 mb30 fs28 c-455a">加载状态</view>
		<view class="flex-box flex-wrap">
			<gt-button class="mr30 mb20" loading type="success"></gt-button>
			<gt-button class="mr30 mb20" loading type="primary" loading-type="spinner"></gt-button>	
			<gt-button class="mr30 mb20" loading type="primary" loading-text="加载中..."></gt-button>
		</view>
		
		<view class="mt20 mb30 fs28 c-455a">图标按钮</view>
		<view class="flex-box flex-wrap">
			<gt-button class="mr30 mb20" icon="sousuo" type="success">按钮</gt-button>
			<gt-button class="mr30 mb20" icon="home" icon-color="#1989fa" plain type="primary">按钮</gt-button>
		</view>
		
		<view class="mt20 mb30 fs28 c-455a">按钮尺寸</view>
		<view>
			<gt-button class="mr30 mb20" type="success" size="large">大按钮</gt-button>
		</view>
		<view class="flex-box flex-wrap">
			<gt-button class="mr30 mb20" type="primary" size="normal">正常按钮</gt-button>
			<gt-button class="mr30 mb20" type="primary" size="small">小按钮</gt-button>
			<gt-button class="mr30 mb20" type="primary" size="mini">迷你按钮</gt-button>
		</view>
		
		
	</view>
</template>

<script>
</script>

<style lang="scss" scoped>
.button {
	padding: 30rpx;
}
</style>
