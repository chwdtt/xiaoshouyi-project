<template>
	<view class="login-custom-setting-wrap">
		<cu-custom bgColor="bg-blue" isBack="true">
			<view slot="content">自定义登录地址</view>
		</cu-custom>
		<view class="custom-setting-content">
			<view class="common-form-input username">
				<input placeholder="请输入名称" v-model="username" placeholder-style="color: rgba(102,102,102,0.8);"/>
			</view>
			<view class="common-form-input">
				<input placeholder="请输入URL" v-model="url" placeholder-style="color: rgba(102,102,102,0.8);"/>
			</view>
			<view class="message-btn">
				<button type="primary" @tap="handleSave">验证并保存</button>
			</view>
		</view>
	</view>
</template>

<script>
	import NavBar from '../../components/NavBar.vue';
	export default {
		components: {
			NavBar
		},
		data() {
			return {
				username: '',
				url: ''
			}
		},
		methods: {
			handleSave() {
				uni.reLaunch({
					url: 'login'
				})
			}
		}
	}
</script>

<style lang="scss" scoped>
	@import '../../static/common.scss';
	.login-custom-setting-wrap {
		/* #ifdef APP-PLUS */
			padding-top: 50upx;
		/* #endif */
		/* #ifdef MP-WEIXIN */
			padding-top: 50upx;
		/* #endif */
		background: #e8e8f1;
		height: $pageHeight;
		overflow-y: hidden;
		
		.username {
			border-bottom: 1px solid $uni-border-color;
		}
		.message-btn {
			margin-top: 30upx;
		}
	}
</style>
