<template>
	<view>
		<view class="top"></view>
		<view class="chu"><p>出发地：{{a}}</p></view>
		<view class="mu"><p>目的地：{{b}}</p></view>
		<view class="yj"><p>预计花费：9999元</p></view>
		<view class="js1"><p>
		　　作为中国历史文化名城，丰富且具有极大的潜能和价值。但是如何将旅游资源作为促进经济的，怎样更好地发展淮南市的将成为我们急需解决的问题。本文通过对淮南市旅游资源现状的分析，以及对现有资源的合理规划，结合市场需求，利用相关旅游资源开发理论，以可持续发展和生态旅游为宗旨，尝试为合理、科学的开发淮南旅游资源提出自己的一些建议和规划。这些建议将对淮南城市发展起到一定的积极作用
			1，促进经济健康可持续发展。有助于优化和调整产业结构。可以增加就业机会，吸纳社会闲散劳动力，有利于维护神会稳定。此外，有关旅游的产业链比较长，可带动其他相关产业的发展。
			2，有利于社会文化融合与传承。淮南旅游资源的开发不仅有利于传统的淮河流域文化的保护，形成独特的文化特色，而且有利于丰富文化内涵，树立良好的城市形象。而且随着现代旅游活动的进行，可促进该地区科技水平的提高和先进文化的吸收。
			3，对环境的积极影响。旅游资源的开发和旅游产业的发展会使得城市环境卫生得以重视和改善。城市和旅游景点的基础设施和服务水平将不断的完善和提高，于此同时居民生活环境也将得以改善，做到人与自然和谐发展。
		</p></view>
	</view>
</template>

<script>
	export default {
		onLoad: function (option) { 
			this.a = option.a;
			this.b = option.b;
			},
		data() {
			return {
				a: "",
				b: ""
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
	.chu{
		width: 100%;
		height: 70rpx;
		display: flex;
		flex-direction: row;
		justify-content: left;
		align-items: center;
	}
	.chu p{
		font-size: 40rpx;
	}
	.mu{
		width: 100%;
		height: 70rpx;
		display: flex;
		flex-direction: row;
		justify-content: left;
		align-items: center;
	}
	.mu p{
		font-size: 40rpx;
	}
	.yj{
		width: 100%;
		height: 70rpx;
		display: flex;
		flex-direction: row;
		justify-content: left;
		align-items: center;
	}
	.yj p{
		font-size: 40rpx;
		color: #F0AD4E;
	}
	.js1{
		width: 100%;
		display: flex;
		flex-direction: row;
		justify-content: left;
		align-items: center;
	}
	.js p{
		font-size: 30rpx;
	}
</style>
