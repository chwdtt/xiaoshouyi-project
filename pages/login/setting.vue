<template>
	<view class="login-setting-wrap">
		<NavBar></NavBar>
	</view>
</template>

<script>
	import NavBar from '@/components/NavBar.vue';
	export default {
		components:{
			NavBar
		},
		data() {
			return {
				
			}
		},
		methods: {
			
		}
	}
</script>

<style lang="scss">
	.login-setting-wrap {
		background: #e8e8f1;
		height: 93.4vh;
		/* #ifdef MP-WEIXIN */
			height: 100vh;
		/* #endif */
	}
</style>
