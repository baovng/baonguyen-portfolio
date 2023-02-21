<script setup>
	import { RouterLink, RouterView } from 'vue-router';
	import HomeView from '@/views/HomeView.vue';
</script>

<template>
	<div class="app">
		<HomeView />
	</div>
</template>

<style>
	.app {
		font-family: 'Avenir', Helvetica, Arial, sans-serif;
		-webkit-font-smoothing: antialiased;
		-moz-osx-font-smoothing: grayscale;
		text-align: center;
		color: #1e1e1e;
	}
</style>
