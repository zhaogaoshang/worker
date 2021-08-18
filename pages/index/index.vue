<template>
	<view class="container">
		<view class="search-box" @tap="handleToSearchResult">
			<icon type="search" size="20" />
			<text class="search-text">搜索</text>
		</view>

		<!-- 今日推荐 -->
		<view class="recommended">
			<view class="recommended-top">
				<uni-row>
					<uni-col :span="12">
						<view class="">
							<view class="item-title">
								今日推荐
							</view>
							<view class="discription">
								近期火热职位
							</view>
						</view>
					</uni-col>
					<uni-col :span="12">
						<view class="right-mony">
							查看更多 >
						</view>
					</uni-col>
				</uni-row>
			</view>
			<view class="recommended-bottom">
				<view class="public-row__aline--center item-box">
					<zgs-jobs class="item-obj" v-for="(item,index) in 12" :key="index"></zgs-jobs>
				</view>
			</view>
		</view>

		<!-- 长期工 -->
		<view class="recommended">
			<view class="recommended-top">
				<uni-row>
					<uni-col :span="12">
						<view class="">
							<view class="item-title">
								长期工
							</view>
							<view class="discription">
								工作时长按月计算
							</view>
						</view>
					</uni-col>
					<uni-col :span="12">
						<view class="right-mony">
							查看更多 >
						</view>
					</uni-col>
				</uni-row>
			</view>
			<view class="recommended-bottom">
				<view class="public-row__aline--center item-box">
					<zgs-jobs class="item-obj" v-for="(item,index) in 12" :key="index"></zgs-jobs>
				</view>
			</view>
		</view>

		<!-- 零时工 -->
		<view class="recommended">
			<view class="recommended-top">
				<uni-row>
					<uni-col :span="12">
						<view class="">
							<view class="item-title">
								零时工
							</view>
							<view class="discription">
								工作时长按天计算
							</view>
						</view>
					</uni-col>
					<uni-col :span="12">
						<view class="right-mony">
							查看更多 >
						</view>
					</uni-col>
				</uni-row>
			</view>
			<view class="recommended-bottom">
				<view class="public-row__aline--center item-box">
					<zgs-jobs class="item-obj" v-for="(item,index) in 12" :key="index"></zgs-jobs>
				</view>
			</view>
		</view>

		<!-- 兼职 -->
		<view class="recommended">
			<view class="recommended-top">
				<uni-row>
					<uni-col :span="12">
						<view class="">
							<view class="item-title">
								兼职
							</view>
							<view class="discription">
								工作时长按小时计算
							</view>
						</view>
					</uni-col>
					<uni-col :span="12">
						<view class="right-mony">
							查看更多 >
						</view>
					</uni-col>
				</uni-row>
			</view>
			<view class="recommended-bottom">
				<view class="public-row__aline--center item-box">
					<zgs-jobs class="item-obj" v-for="(item,index) in 12" :key="index"></zgs-jobs>
				</view>
			</view>
		</view>

	</view>
</template>

<script>
	export default {
		data() {
			return {

			};
		},

		onLoad() {
			uni.setNavigationBarTitle({
				title: '献县'
			})
		},

		methods: {
			// 搜索结果页面
			handleToSearchResult() {
				uni.navigateTo({
					url: '../searchResult/searchResult'
				})
			}
		}
	}
</script>

<style lang="scss" scoped>
	.search-box {
		@extend .public-row__center;
		margin: 30rpx;
		border: 2rpx solid $theme-hui;
		border-radius: 10rpx;
		height: 60rpx;
		white-space: 10rpx;
		font-size: $f30;
	}

	.search-text {
		margin-left: 10rpx;
		font-weight: 600;
		color: #666;
	}

	.recommended {
		font-size: $f26;
		font-weight: 500;
		background-color: #fff;
		padding: 30rpx 0;
		margin-bottom: 30rpx;

		.recommended-top {
			padding: 0 30rpx 0 30rpx;

			.discription {
				font-size: $f22;
				margin: 10rpx 0;
			}
		}

		.right-mony {
			text-align: right;
		}

		.item-title {
			font-size: $f30;
			font-weight: 600;
			color: $theme-red;
		}

		.recommended-bottom {
			.item-obj {
				margin-left: 30rpx;
			}

			.item-box {
				overflow-x: scroll;
			}
		}
	}
</style>
