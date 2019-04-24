<template>
	<view class="register-wrap">
		<view class="register-info">注册成功后将获取30天免费试用</view>
		<view class="register-content">
			<view class="username">
				<input :placeholder="placeholder" v-model="username" placeholder-style="color: rgba(102,102,102,0.8);"/>
			</view>
			<view class="message-btn">
				<button type="primary">获取验证码</button>
			</view>
		</view>
		<view class="email-box">
			<navigator open-type="navigate" url="regsiter?id=2">用邮箱注册</navigator>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				id: 1,
				username: '',
				placeholder: '输入手机号'
			}
		},
		onLoad(options) {
			this.id = Number(options.id);
			if(this.id !== 1){
				this.placeholder = '输入邮箱'
			}
		},
		methods: {
			
		}
	}
</script>

<style lang="scss">
	.register-wrap {
		display: flex;
		flex-direction: column;
		background: #e8e8f1;
		height: 93.4vh;
		/* #ifdef MP-WEIXIN */
			height: 100vh;
		/* #endif */
		.register-info {
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
		.register-content {
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
