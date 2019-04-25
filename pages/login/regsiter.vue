<template>
	<view class="register-wrap">
		<cu-custom bgColor="bg-blue" isBack="true">
			<view slot="content">新用户注册</view>
		</cu-custom>
		<view class="register-info">注册成功后将获取30天免费试用</view>
		<view class="register-content">
			<view class="username common-form-input">
				<input :placeholder="placeholder" v-model="username" placeholder-style="color: rgba(102,102,102,0.8);"/>
			</view>
			<view class="message-btn">
				<button class="bg-blue">获取验证码</button>
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

<style lang="scss" scoped>
	@import '../../static/common.scss';
	.register-wrap {
		display: flex;
		height: $pageHeight;
		flex-direction: column;
		.register-info {
			font-size: 28upx;
			text-align: left;
			padding: 30upx 4%;
			color: $alphaBlack8;
		}
		.message-btn {
			padding: 0 4%;
			margin-top: 30upx;
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
