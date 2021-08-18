<template>
	<view class="jobs-box">
		<view class="jobs">
			<image class="jobs-image"
				src="https://q-extra.paixin.com/default/2021/0705/c6f1f445c4fd132f153d38c1ec62c085.jpg?imageView2/2/format/webp"
				mode="">
			</image>
			<view class="jobs-name">电焊电焊电焊电焊电焊</view>
			<view class="price">1000元/月</view>
		</view>
	</view>
</template>

<script>
	export default {
		name: "zgs-jobs",
		data() {
			return {

			};
		}
	}
</script>

<style lang="scss" scoped>
	.jobs-box {
		display: inline-block;

		.jobs {
			@extend .public-column;
			width: 240rpx;

			.jobs-image {
				width: 240rpx;
				height: 240rpx;
				border-radius: 10rpx;
			}

			.jobs-name {
				font-size: $f28;
				font-weight: 600;
				width: 240rpx;
				margin: 10rpx 0;
				overflow: hidden;
				text-overflow: ellipsis;
				white-space: nowrap;
			}

			.price {
				font-size: $f26;
				color: $theme-red;
			}
		}
	}
</style>
