<template>
	<view class="login-setting-wrap">
		<view class="status_bar">
        </view>
		<NavBar title="设置登录地址" leftText="取消" icon="+" url="login"></NavBar>
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
	.status_bar {
        height: var(--status-bar-height);
        width: 100%;
    }
	.login-setting-wrap {
		background: #e8e8f1;
		height: $pageHeight;
		overflow-y: hidden;
		.setting-list {
			margin-top: 24upx;
			view.list {
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
			margin-right: -14upx;
		}
	}
</style>
