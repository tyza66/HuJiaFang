<template>
	<view>
		<view class="top"></view>
		<view class="title">
			<view class="left">
				<view class="p1"><image src="../../static/icons/wei.png"></image><p>锦州</p></view>
				<view class="p2"><p>您好，Admin</p></view>
			</view>
			<view class="right">
				<view>
					<image src="../../static/icons/she.png"></image>
					<p>设置</p>
				</view>
				<view>
					<image src="../../static/icons/fa.png"></image>
					<p>发现</p>
				</view>
			</view>
		</view>
		<view class="swiper-c">
			<swiper indicator-dots="true" autoplay="autoplay" interval="1000" duration="500">
				<swiper-item>
					<image src="../../static/picture/pi6.png"></image>
				</swiper-item>
				<swiper-item>
					<image src="../../static/picture/pi7.png"></image>
				</swiper-item>
				<swiper-item>
					<image src="../../static/picture/pi8.png"></image>
				</swiper-item>
				<swiper-item>
					<image src="../../static/picture/pi9.png"></image>
				</swiper-item>
				<swiper-item>
					<image src="../../static/picture/pi10.png"></image>
				</swiper-item>
			</swiper>
		</view>
		<view class="lvtu">
			<p class="b">旅途规划</p>
			<view class="i1"><p>出发地：</p><input type="text" v-model="chufa"></view>
			<view class="i2"><p>目的地：</p><input type="text" v-model="mudi"></view>
			<view class="i3" @click="chaxun()"><p>查询</p></view>
		</view>
		<view class="tuijian">
			<p class="b">推荐项目</p>
			<view class="i11">
				<view class="high1"><p>·情侣项目</p></view>
				<view class="high2">
					<view class="xiao"><p class="l">鬼屋冒险：这里约会的好处是有惊心动魄的氛围。</p><p class="r"><u>了解一下</u></p></view>
					<view class="xiao"><p class="l">私人影院：两个人看电影，环境好，不会被别打扰。</p><p class="r"><u>了解一下</u></p></view>
					<view class="xiao"><p class="l">ktv包房：一起发泄生活中的开心与不开心。</p><p class="r"><u>了解一下</u></p></view>
				</view>
			</view>
			<view class="i22">
				<view class="high1"><p>·家庭项目</p></view>
				<view class="high2">
					<view class="xiao"><p class="l">跟团旅游：简简单单只要人去就行说走就走的旅行。</p><p class="r"><u>了解一下</u></p></view>
					<view class="xiao"><p class="l">自驾定制：自驾路线，沿途信息，疫情明细。</p><p class="r"><u>了解一下</u></p></view>
					<view class="xiao"><p class="l">组团随行：这里约会的好处是有惊心动魄的氛围。</p><p class="r"><u>了解一下</u></p></view>
				</view>
			</view>
			<view class="i33">
				<view class="high1"><p>·聚会项目</p></view>
				<view class="high2">
					<view class="xiao"><p class="l">棋牌娱乐：安全，可靠，舒适的棋牌场所。</p><p class="r"><u>了解一下</u></p></view>
					<view class="xiao"><p class="l">狼人游戏：桌游，六七人以上，良好的揣测能力。</p><p class="r"><u>了解一下</u></p></view>
					<view class="xiao"><p class="l">热血运动：对外出租运动场信息大全。</p><p class="r"><u>了解一下</u></p></view>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				chufa:"锦州市渤海大学滨海校区",
				mudi:""
			}
		},
		methods: {
				chaxun(){
					uni.navigateTo({
						url:"../chaxun/chaxun"+"?a="+this.chufa+"&b="+this.mudi
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
	.title{
		height: 180rpx;
		width: 100%;
	}
	.left{
		float: left;
		width: 400rpx;
		height: 160rpx;
		margin-top: 10rpx;
		display: flex;
		flex-direction: column;
		justify-content: left;
		align-items: left;
	}
	.p1{
		margin-left: 20rpx;
		height: 80rpx;
		display: flex;
		flex-direction: row;
		justify-content: left;
		align-items: center;
	}
	.p1 image{
		width: 50rpx;
		height: 50rpx;
	}
	.p1 p{
		display: inline;
		font-size: 36rpx;
		font-weight: 550;
	}
	.p2{
		margin-left: 20rpx;
		height: 50rpx;
		display: flex;
		flex-direction: row;
		justify-content: left;
		align-items: center;
	}
	.p2{
		color: #999999;
		font-size: 35rpx;
	}
	.right{
		float: right;
		width: 220rpx;
		height: 160rpx;
		margin-top: 10rpx;
		display: flex;
		flex-direction: row;
		justify-content: left;
		align-items: center;
	}
	.right view{
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		margin: 0 auto;
	}
	.right view image{
		width: 80rpx;
		height: 80rpx;
	}
	.right view p{
		font-weight: 500;
	}
	.swiper-c{
		width: 100%;
		height: 400rpx;
	}
	.swiper-c swiper{
		width: 100%;
		height: 100%;
	}
	.swiper-c swiper swiper-item image{
		width: 100%;
		height: 100%;
	}
	.lvtu{
		position: relative;
		width: 96%;
		height: 260rpx;
		margin: 0 auto;
		margin-top: 10rpx;
		border-radius: 10rpx;
		background: #F1F1F1;
	}
	.b{
		position: absolute;
		left:15rpx;
		top: 5rpx;
		font-size: 60rpx;
		font-family: "幼圆";
		font-weight: 500;
	}
	.i1{
		position: absolute;
		width: 90%;
		height: 85rpx;
		top: 75rpx;
		left: 40rpx;
		border-radius: 45rpx;
		background: #FFFFFF;
		display: flex;
		flex-direction: row;
		justify-content: center;
		align-items: center;
	}
	.i2{
		position: absolute;
		width: 90%;
		height: 85rpx;
		top: 165rpx;
		left: 40rpx;
		border-radius: 45rpx;
		background: #FFFFFF;
		display: flex;
		flex-direction: row;
		justify-content: center;
		align-items: center;
	}
	.i3{
		position: absolute;
		width: 120rpx;
		height: 65rpx;
		top: 5rpx;
		left: 560rpx;
		border-radius: 45rpx;
		background: #F0AD4E;
		display: flex;
		flex-direction: row;
		justify-content: center;
		align-items: center;
	}
	.i11{
		position: absolute;
		width: 90%;
		height: 200rpx;
		top: 75rpx;
		left: 40rpx;
		display: flex;
		flex-direction: column;
		justify-content: top;
		align-items: center;
	}
	.i22{
		position: absolute;
		width: 90%;
		height: 200rpx;
		top: 280rpx;
		left: 40rpx;
		display: flex;
		flex-direction: column;
		justify-content: top;
		align-items: center;
	}
	.i33{
		position: absolute;
		width: 90%;
		height: 200rpx;
		top: 485rpx;
		left: 40rpx;
		display: flex;
		flex-direction: column;
		justify-content: top;
		align-items: center;
	}
	.tuijian{
		position: relative;
		width: 96%;
		height: 680rpx;
		margin: 0 auto;
		margin-top: 10rpx;
		background: #F1F1F1;
	}
	.high1{
		width: 100%;
		height: 70rpx;
		display: flex;
		flex-direction: row;
		justify-content: left;
		align-items: center;
	}
	.high1 p{
		font-size: 35rpx;
		font-family: "幼圆";
		font-weight: 500;
	}
	.high2{
		width: 100%;
		height: 100%;
	}
	.high2 .xiao{
		height: 33%;
		width: 100%;
		display: flex;
		flex-direction: row;
		justify-content: left;
		align-items: center;
	}
	.high2 .xiao .l{
		float: left;
		font-size: 10rpx;
	}
	.high2 .xiao .r{
		float: right;
		font-size: 10rpx;
		color: #009EE7;
	}
</style>
