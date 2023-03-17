<script setup>
	import { RouterLink, RouterView } from 'vue-router';
</script>

<template>
	<div class="app">
		<router-view />
	</div>
</template>

<style>
	.app {
		font-family: 'Avenir', Helvetica, Arial, sans-serif;
		-webkit-font-smoothing: antialiased;
		-moz-osx-font-smoothing: grayscale;
		text-align: center;
	}
</style>
