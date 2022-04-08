<template>
	<view>
		<view class="top"></view>
		<view class="bg"></view>
		<view class="ic">
			<h3>户嘉方</h3>
			<p>你的旅行伴侣.</p>
		</view>
		<view class="login">
			<view class="item">
				<image src="../../static/icons/zhanghao.png"></image>
				<input type="text" placeholder="手机号码"/>
			</view>
			<view class="item">
				<image src="../../static/icons/mima.png"></image>
				<input type="password" placeholder="设置密码"/>
			</view>
			<view class="item">
				<image src="../../static/icons/mima.png"></image>
				<input type="password" placeholder="重复密码"/>
			</view>
			<view class="item">
				<image src="../../static/icons/mima.png"></image>
				<input type="password" placeholder="短信验证码" v-model="pass"/>
			</view>
			<view class="item" @click="yanzheng()">
				<h2>获取验证码</h2>
			</view>
			<view class="item" @click="denglu()">
				<h2>注册</h2>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				pass:""
			}
		},
		onLoad() {

		},
		methods: {
			denglu(){
				if(this.pass=="1234"){
					uni.switchTab({
						url:"../shouye/shouye"
					})
				}else{
					uni.showToast({
						image:"../../static/wrong.png",
						title:"验证码错误"
					})
				}
			},
			yanzheng(){
				uni.showToast({
					title:"验证码已发送"
				})
			}
		}
	}
</script>

<style>
	.top {
		height: var(--status-bar-height);
		width: 100%;
		background-color: #FFFFFF;
	}
	.bg{
		width: 100%;
		height: 100%;
		position: absolute;
		background-image: linear-gradient(to bottom right, #009EE7, yellow);
	}
	.ic{
		position: relative;
		top: 220rpx;
		width: 100%;
		height: 200rpx;
		z-index: 2000;
	}
	.ic h3{
		font-size: 100rpx;
		font-family: "幼圆";
		font-weight: 1000;
		margin: 0 auto;
		text-align: center;
	}
	.ic p{
		font-size: 50rpx;
		color: ##C8C7CC;
		font-family: "幼圆";
		margin: 0 auto;
		text-align: center;
	}
	.login{
		position: relative;
		width: 500rpx;
		top: 300rpx;
		margin: 0 auto;
	}
	.login .item{
		display: flex;
		flex-direction: row;
		justify-content: center;
		align-items: center;
		width: 100%;
		height: 100rpx;
		background: rgb(0,0,0,0.3);
		border-radius: 45rpx;
		margin-top: 10rpx;
		
	}
	.login .item image{
		width: 80rpx;
		height: 80rpx;
	}
</style>
