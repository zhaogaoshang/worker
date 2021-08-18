<template>
	<view class="container international">

	</view>
</template>

<script>
	export default {
		data() {
			return {

			};
		},

		onLoad() {

		},

		onShow() {
			uni.setNavigationBarColor({
				frontColor: '#ffffff',
				backgroundColor: '#13227a',
				animation: {
					duration: 40,
					timingFunc: 'easeIn'
				}
			})
		}
	}
</script>

<style lang="scss">
	.international {
		background-color: $theme-lan;
	}
</style>
