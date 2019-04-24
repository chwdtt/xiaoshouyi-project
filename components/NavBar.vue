<template>
	<view class="nav-bar">
		<view class="back">
			<navigator url="login">取消</navigator>
		</view>
		<view class="title">设置登录地址</view>
		<view class="custom-address">+</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			};
		}
	}
</script>

<style lang="scss">
	.nav-bar {
		position: fixed;
		left: 0;
		width: 94%;
		height: 45px;
		display: flex;
		justify-content: space-between;
		align-items: center;
		color: #333;
		background: #fff;
		padding: 7upx 3%;
		font-size: 30upx;
		.back {
			color: #007aff;
			font-size: 24upx;
		}
		.custom-address {
			color: #007aff;
			font-size: 40upx;
		}
	}
</style>
