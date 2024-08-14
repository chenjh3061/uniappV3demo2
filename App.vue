<template>
	<GlobalFooterVue />
</template>
<script>
	export default {
		onLaunch: function() {
			console.log('App Launch')
		},
		onShow: function() {
			console.log('App Show')
		},
		onHide: function() {
			console.log('App Hide')
		}
	}
	import GlobalFooterVue from './pages/components/GlobalFooter.vue'
</script>

<style>
	/*每个页面公共css */
</style>
