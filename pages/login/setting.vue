<template>
	<view class="login-setting-wrap">
		<cu-custom bgColor="bg-blue" isBack="true">
			<view slot="content">设置登录地址</view>
			<view slot="right">
				<navigator class="custom-address" url="customSetting">+</navigator>
			</view>
		</cu-custom>
		<view class="setting-list">
			<radio-group @change="radioChange">
				<view class="list" v-for="(item, index) in items" :key="item.value">
					<text>{{item.name}}</text>
					<radio class="radio-box" :value="item.value" :checked="index === current" />
				</view>
			</radio-group>
        </view>
	</view>
</template>

<script>
	import NavBar from '@/components/NavBar.vue';
	export default {
		onLaunch: function() {
			
		},
		components:{
			NavBar
		},
		data() {
			return {
				items: [{
                    value: 'USA',
                    name: '销售易'
                },
                {
                    value: 'CHN',
                    name: '中国',
                    checked: 'true'
                },
                {
                    value: 'BRA',
                    name: '巴西'
                },
                {
                    value: 'JPN',
                    name: '日本'
                },
                {
                    value: 'ENG',
                    name: '英国'
                },
                {
                    value: 'FRA',
                    name: '法国'
                },
            ],
            current: 0
			}
		},
		methods: {
			radioChange: function(evt) {
				for (let i = 0; i < this.items.length; i++) {
					if (this.items[i].value === evt.target.value) {
						this.current = i;
						break;
					}
				}
			}
		}
	}
</script>

<style lang="scss" scoped>
	@import '../../static/common.scss';
	.login-setting-wrap {
		background: #e8e8f1;
		height: $pageHeight;
		overflow-y: hidden;
		.setting-list {
			margin-top: 24upx;
			radio-group {
				width: 100%;
			}
			view.list {
				width: 100%;
				display: flex;
				height: 80upx;
				background: #fff;
				justify-content: space-between;
				align-items: center;
				padding: 0 20upx;
				font-size: 30upx;
				border-bottom: 1px solid #ccc;
			}
		}
		.radio-box {
		}
		.custom-address {
			font-size: 58upx;
			margin-right: 26upx;
		}
	}
</style>
