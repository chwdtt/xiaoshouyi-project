<template>
	<view class="nav-bar">
		<view class="back">
			<navigator open-type="reLaunch" :url="url">{{leftText}}</navigator>
		</view>
		<view class="title">{{title}}</view>
		<navigator class="custom-address" url="customSetting" v-if="icon !== 'false'">{{icon}}</navigator>
		<navigator class="custom-address" url="customSetting" v-else style="margin-left: 40upx"> </navigator>
	</view>
</template>

<script>
	export default {
		props: {
			title: String,
			leftText: String,
			icon: String,
			url: String
		},
		data() {
			return {
				
			};
		},
		methods:{
			
		}
	}
</script>

<style lang="scss">
	.nav-bar {
		width: 94%;
		height: 38px;
		display: flex;
		justify-content: space-between;
		align-items: center;
		color: #333;
		background: #fff;
		padding: 7upx 3%;
		font-size: 30upx;
		.title {
			font-size: 36upx;
			font-weight: 200;
		}
		.back {
			color: #007aff;
			font-size: 32upx;
		}
		.custom-address {
			color: #007aff;
			position: relative;
			/* #ifdef H5 */
				margin-right: -1px;
				font-size: 60upx;
			/* #endif */
			/* #ifdef APP-PLUS */
				font-size: 70upx;
			/* #endif */
			/* #ifdef MP-WEIXIN */
				font-size: 70upx;
			/* #endif */
		}
	}
</style>
