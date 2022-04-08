<template>
	<view>
		<view class="top"></view>
		<view class="someting">
			<image src="../../static/picture/shangpin1.png"></image>
			<p>武汉-樱花胸针</p>
			<p class="jia">￥999</p>
		</view>
		<view class="someting">
			<image src="../../static/picture/shangpin2.png"></image>
			<p>敦煌-莫高窟陶瓷杯垫</p>
			<p class="jia">￥999</p>
		</view>
		<view class="someting">
			<image src="../../static/picture/shangpin3.png"></image>
			<p>杭州-桂花香水</p>
			<p class="jia">￥999</p>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		methods: {
			
		}
	}
</script>

<style>
.top {
		height: var(--status-bar-height);
		width: 100%;
		background-color: #FFFFFF;
	}
	.someting{
		position: relative;
		width: 100%;
		height: 180rpx;
		border-bottom: #000000 solid 1rpx;
	}
	.someting image{
		width: 150rpx;
		height: 150rpx;
		margin-top: 15rpx;
		margin-left: 15rpx;
	}
	.someting p{
		position: absolute;
		top: 60rpx;
		left: 180rpx;
		font-size: 40rpx;
		width: 580rpx;
		height: 50rpx;
	}
	.someting .jia{
		position: absolute;
		width: 580rpx;
		height: 50rpx;
		font-size: 40rpx;
		top: 60rpx;
		color: gold;
		left: 580rpx;
	}
</style>
