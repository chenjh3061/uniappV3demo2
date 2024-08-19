<template>
	<view>
		<view>往期文章</view>
		<view class="post-list" v-for="(post, index) in postList" :key="post.id">
			<view>{{ post.id }}</view>
			<view>{{ post.text }}</view>
		</view>
	</view>
</template>

<script setup>
import { ref } from 'vue';

const postList = ref([
	{id:1, text:"123123123"},
	{id:2, text:"123123123"},
	{id:3, text:"123123123"},
	{id:4, text:"123123123"},
])
console.log(postList.value);
</script>

<style scoped>
.post-list {
	border: 1rpx;
}
</style>