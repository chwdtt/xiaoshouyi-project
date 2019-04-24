<template>
	<view class="forget-password-wrap">
		<view class="forget-password-info">找回密码功能将停用您当前的密码，请在验证身份后设置新密码</view>
		<view class="forget-password-content">
			<view class="username">
				<input placeholder="输入登录账户(手机号/邮箱)" v-model="username" placeholder-style="color: #333;font-size: 30upx"/>
			</view>
			<view class="message-btn">
				<button type="primary">获取验证码</button>
			</view>
		</view>
		<view class="email-box">
			<navigator url="">用邮箱注册</navigator>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				username: ''
			}
		},
		methods: {
			
		}
	}
</script>

<style lang="scss">
	.forget-password-wrap {
		display: flex;
		flex-direction: column;
		background: #e8e8f1;
		height: 93.4vh;
		/* #ifdef MP-WEIXIN */
			height: 100vh;
		/* #endif */
		.forget-password-info {
			font-size: 28upx;
			text-align: left;
			padding: 30upx 4%;
			color: rgba($color: #666, $alpha: 0.8);
		}
		.username {
			width: 100%;
			height: 90upx;
			display: flex;
			align-items: center;
			background-color: #fff;
			padding: 0 4%;
			margin-bottom: 26upx;
			input {
				width: 100%;
				height: 50upx;
				color: #666;
				font-weight: 200;
				font-size: 28upx;
			}
		}
		.message-btn {
			padding: 0 4%
		}
		.forget-password-content {
			flex: 12;
		}
		.email-box {
			text-align: center;
			flex: 1;
			color: #007aff;
			font-size: 28upx;
		}
	}
</style>
