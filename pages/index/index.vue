<template>
	<view>
		<view id="headTitle">音悦小小屋</view>
		<navigator url="../demo1/demo1" hover-class="navigator-hover">
			<button type="default">跳转到新页面</button>
		</navigator>
		<view>
			<swiper :indicator-dots="true" :autoplay="true" :interval="3000" :duration="1000">
				<swiper-item v-for="(item, index) in topSwiper" :key="index">
					<view class="swiper-item">{{ item }}</view>
				</swiper-item>
			</swiper>
		</view>
		<button v-on:click="addNum">
			<view :style="{background:color}">{{ num }}</view>
		</button>
		<view class="daily-recommand">
			<text selectable>每日推荐</text>
			<scroll-view scroll-x="true" class="scrollView">
				<view class="box" v-for="(item, index) in dailyRecommand" :kry="index">
					{{ item }}
				</view>
			</scroll-view>
		</view>
		<view class="selected">
			<view>专题精选</view>
		</view>

		<GlobalFooter />
	</view>
</template>
<script setup>
	import {
		ref,
		onMounted,
		watchEffect
	} from 'vue';
	import GlobalFooter from '../components/GlobalFooter.vue';

	const topSwiper = [11111, 22222, 33333, 44444, 55555];

	const num = ref(0);
	const color = ref("#fc359a");
	const addNum = () => {
		num.value++;
		color.value = "#" + String(Math.random()).substring(3, 9)
	};

	setInterval(() => {
		if (num.value > 0) {
			num.value--;
			color.value = "#" + String(Math.random()).substring(3, 9)
		}
	}, 1000);

	const dailyRecommand = ["图片1", "图片2", "图片3", "图片4", "图片5", "图片6"]

	onMounted(() => {
		// 组件加载时执行的逻辑

	});
</script>

<style lang="scss">
	swiper {
		border: #000 2px;
		width: 100vw;
	}

	.swiper-item {
		border: #000;
	}

	#headTitle {
		margin: 0 0 0 40vw;
		color: #000;
	}

	.scrollView {
		width: 80%;
		height: 220px;
		border: 1px solid #000;
		white-space: nowrap;

		.box {
			width: 100px;
			height: 100px;
			background-color: aqua;
			display: inline-block;
			margin: 5px;
			border-radius: 5;
		}
	}
</style>