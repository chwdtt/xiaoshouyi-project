<template>
	<view class="experience-wrap">
		<view class="experience-info">验证手机号，即可进入模拟演示环境，尽情体验销售易的功能</view>
		<view class="experience-content">
			<view class="username">
				<input placeholder="手机号/邮箱" v-model="username" placeholder-style="color: #333;font-size: 30upx"/>
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
				username:''
			}
		},
		methods: {
			
		}
	}
</script>

<style lang="scss" scoped>
	@import '../../static/common.scss';
	.experience-wrap {
		display: flex;
		flex-direction: column;
		background: #e8e8f1;
		height: $pageHeight;
		/* #ifdef H5 */
			height: $pageHeightAndH5;
		/* #endif */
		.experience-info {
			font-size: 28upx;
			text-align: left;
			padding: 30upx 4%;
			color: $alphaBlack8;
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
		.experience-content {
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
