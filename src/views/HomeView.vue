<template>
	<div class="logo-container" v-if="showLogo">
		<div class="logo-animation">
			<LogoAnimation />
		</div>
	</div>
	<div class="content-container" v-else>
		<About />
	</div>
</template>

<script>
	import LogoAnimation from '../components/LogoAnimation.vue';
	import About from '@/components/About.vue';
	export default {
		components: {
			LogoAnimation,
			About,
		},
		data() {
			return {
				showLogo: true,
			};
		},
		mounted() {
			setTimeout(() => {
				this.showLogo = false;
			}, 3000); // Change 3000 to the duration of your logo animation in milliseconds
		},
	};
</script>

<style>
	.logo-container,
	.content-container {
		display: flex;
		justify-content: center;
		align-items: center;
		height: 100vh;
	}

	.logo-container {
		color: #fff;
		font-size: 4rem;
	}

	.content-container {
		font-size: 3rem;
		color: #fff;
	}
</style>
