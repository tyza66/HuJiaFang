<template>
	<view>
		<view class="top"></view>
		<view class="dongtai" v-for="(item,i) in dt">
			<view class="user"><image :src="item[0]"><p>{{item[1]}}</p></view>
			<view class="xiaoxi">{{item[2]}}</view>
		</view>
		<view class="jia" @click="chu()"><p>+</p></view>
		<view class="shi" v-show="xian">
			<view class="shuru">
				<textarea v-model="out"></textarea>
			</view>
			<view class="tijiao" @click="toa()">发送</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				xian: false,
				out:"",
					dt:[
						["../../static/icons/ll.png","徒步阿龙","到达世界最高城！理塘！太美了理塘，我们来看看那边的山吧！"],
						["../../static/icons/tt1.png","六道轮回","们这一生，注定有很多偶遇，偶遇一件事，偶遇某个人，让我们的生活多了许多曲折。不管怎样，总有那么几件事，让你念念不忘，总有那么一个人，让你陡生叹惜。错过的，就当是路过吧，遗忘是彼此最好的怀念。一路走来，偶遇的星光，让我们有遗憾，亦有温暖。"],
						["../../static/icons/tt2.png","饕餮少女","我就像现在一样看着你微笑，沉默，得意，失落，于是我跟着你开心也跟着你难过，只是我一直站在现在而你却永远停留过去。"],
						["../../static/icons/tt3.png","一夜奈良山","如此我便该好好的活着，用自己最喜欢的方式活着，无谓他人的闲言碎语。一辈子太短，我不想等到老了的时候再后悔，原来我没有年轻过。"],
						["../../static/icons/tt4.png","若即若离","酒像女人，在酒里同样也有人生得失，成功的女人，可以觥筹交错，生活中绝不让须眉。失意的女人，香腮含泪，举起酒杯一个人醉。"],
						["../../static/icons/tt5.png","陪你演戏","每个睡不着的夜晚，我都在想你。空气中的气流是你的呼吸，被子是你的怀抱，弥漫的花香是你的味道。怀里抱着自己，亦是抱着你。"],
						["../../static/icons/tt6.png","牛奶煮萝莉","不再打扰，只是守候;不再联系，只是铭记。爱过的人，谁能忘;用心的情，谁不疼。不愿醒的美梦，最是难成;忘不了的感情，最是心疼!"],
						["../../static/icons/tt7.png","陈情匿旧酒","多想把自己遗忘在角落不被人想起，也不想起任何的人。不看，不想，不去观望。静静地呆着。不去伤心与难过如今的自己连喝醉酒的勇气都没有了。如今的我还剩下什么。"],
						["../../static/icons/tt8.png","嘴角的樱桃汁","心里有你的人，总会主动找你。心里没有你的人，总是自动忽略你。其实，沉默就是答案，躲闪就是答案，不再主动就是答案，其实，你早该明白了。"]
					]
				}
		},
		methods: {
			chu(){
				this.xian = !this.xian;
			},
			toa(){
				var a = [["../../static/icons/ww.png","Admin",this.out]];
				this.dt = this.dt.concat(a);
				uni.showToast({
				    title: '发布成功',
				    duration: 2000
				});
				this.out = "";
				this.xian = !this.xian;
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
	.dongtai{
		width: 100%;
	}
	.dongtai .user{
		height: 100rpx;
		display: flex;
		flex-direction: row;
		justify-content: left;
		align-items: cneter;
	}
	.dongtai .user image{
		width: 100rpx;
		height: 100rpx;
		border-radius: 50rpx;
		margin-left: 30rpx;
	}
	.dongtai .user p{
		font-size: 60rpx;
		height: 30rpx;
		margin-top: 10rpx;
	}
	.xiaoxi{
		width: 80%;
		margin: 0 auto;
	}
	.jia{
		position: fixed;
		z-index: 1000;
		right: 10rpx;
		top: 1100rpx;
		width: 100rpx;
		height: 100rpx;
		border-radius: 50rpx;
		background: #FFD700;
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: cneter;
	}
	.jia p{
		margin: 0 auto;
		margin-top: -40rpx;
		width: 50rpx;
		height: 50rpx;
		font-size: 60rpx;
		text-align: center;
	}
	.shi{
		position: fixed;
		z-index: 500;
		left: 25rpx;
		top: 700rpx;
		width: 700rpx;
		height: 300rpx;
		border-radius: 30rpx;
		background: #FFD700;
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: cneter;
	}
	.shuru{
		width: 600rpx;
		height:	300rpx;
		margin: 0 auto;
		margin-top: 50rpx;
		background: #C8C7CC;
	}
	.shuru textarea{
		width: 100%;
		height: 100%;
	}
	.tijiao{
		width: 140rpx;
		margin: 0 auto;
		text-align: center;
		background: red;
		border: #000000 solid 1px;
		border-radius: 5rpx;
	}
</style>
