<template>
	<view>
		<cu-custom bgcolor="bg-white" :isBack="true">
			<block slot="content">余额</block>
			<block slot="right">
				<navigator url="/pages/user/detail">
				<view class="margin-right-sm">
				明细	
				</view>
				</navigator>
				</block>
		</cu-custom>
		<view class="flex justify-center align-center main">
			<view class="text-center basis-df">
				<view class="text-grey margin-bottom-sm">我的余额</view>
				<view class="text-bold text-xxl">￥2568.00</view>
			</view>
			<view class="text-center basis-df">
				<view class="text-grey margin-bottom-sm">今日收益</view>
				<view class="text-bold text-xxl">￥568.00</view>
			</view>
		</view>
		<view class="padding">
			<button class="cu-btn block lg bg-orange margin-bottom-sm" @click="balance">充值</button>
			<button class="cu-btn block lg bg-green" @click="deposit">提现</button>
			<navigator class="bind text-center margin-top-xl" url="/pages/user/bind">绑定提现账号</navigator>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {

			};
		},
		methods: {
			balance() {
				uni.navigateTo({
					url: '/pages/user/recharge'
				})
			},
			deposit() {
				uni.navigateTo({
					url: '/pages/user/deposit'
				})
			}
		}
	}
</script>

<style lang="scss">
.main {
	height: 400rpx;
}
.bind {
	text-decoration: underline;
}
</style>
