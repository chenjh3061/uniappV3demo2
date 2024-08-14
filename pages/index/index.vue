<template>
	<view>
		<view id="headTitle">音悦小小屋</view>
		<navigator url="../demo1/demo1" hover-class="navigator-hover">
			<button type="default">跳转到新页面</button>
		</navigator>
		<view>
			<swiper :indicator-dots="true" :autoplay="true" :interval="3000" :duration="1000">
				<swiper-item>
					<view class="swiper-item">11111</view>
				</swiper-item>
				<swiper-item>
					<view class="swiper-item">22222</view>
				</swiper-item>
			</swiper>
		</view>
		<view class="box" hover-class="boxHover">
			view布局标签
			<view class="inner" hover-class="innerHover" hover-stop-propagation>二号标签</view>
			<datalist></datalist>
		</view>
		<view class="text">
			<text selectable>这里是text文本</text>
		</view>
		<scroll-view scroll-x="true" class="scrollView">
			<view class="box">scroll子元素</view>
			<view class="box">scroll子元素</view>
			<view class="box">scroll子元素</view>
			<view class="box">scroll子元素</view>
			<view class="box">scroll子元素</view>
			<view class="box">scroll子元素</view>
			<view class="box">scroll子元素</view>
			<view class="box">scroll子元素</view>
			<view class="box">scroll子元素</view>
			<view class="box">scroll子元素</view>
			<view class="box">scroll子元素</view>
			<view class="box">scroll子元素</view>
			<view class="box">scroll子元素</view>
			<view class="box">scroll子元素</view>
			<view class="box">scroll子元素</view>
			<view class="box">scroll子元素</view>
			<view class="box">scroll子元素</view>
			<view class="box">scroll子元素</view>
		</scroll-view>
		
		<GlobalFooter />
	</view>
</template>
<script setup>
	import {
		ref,
		onMounted
	} from 'vue';
	import GlobalFooter from '../components/GlobalFooter.vue';

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
		}
	}

	.box {
		width: 200px;
		height: 200px;
		background: #ccc;
	}

	.boxHover {
		background: orange;
		width: 300px;
	}

	.inner {
		width: 150px;
		height: 150px;
		background: green;
	}

	.innerHover {
		background: greenyellow;
	}
</style>