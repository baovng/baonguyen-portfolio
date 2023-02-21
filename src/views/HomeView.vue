<template>
	<div class="logo-container" v-if="showLogo">
		<div class="logo-animation">
			<LogoAnimation />
		</div>
	</div>
	<div class="hello-container" v-else>
		<p>Hi, I'm Bao Nguyen</p>
	</div>
</template>

<script>
	import LogoAnimation from '../components/LogoAnimation.vue';
	export default {
		components: {
			LogoAnimation,
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
	.hello-container {
		display: flex;
		justify-content: center;
		align-items: center;
		text-align: center;
		height: 100vh;
	}

	.logo-container {
		color: #fff;
		font-size: 4rem;
	}

	.hello-container {
		font-size: 3rem;
		color: #fff;
	}
</style>
