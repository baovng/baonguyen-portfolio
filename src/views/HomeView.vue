<template>
	<div class="logo-container vh-100" v-if="showLogo">
		<div class="logo-animation">
			<LogoAnimation />
		</div>
	</div>
	<div class="content-container d-flex flex-column" v-else>
		<section>
			<Intro />
		</section>
		<section>
			<About />
		</section>
		<section class="mt-5">
			<Experience />
		</section>
		<section>
			<Project />
		</section>
		<section>
			<Footer />
		</section>
	</div>
</template>

<script>
	import LogoAnimation from '../components/LogoAnimation.vue';
	import About from '@/components/About.vue';
	import Intro from '@/components/Intro.vue';
	import Experience from '@/components/Experience.vue';
	import Project from '@/components/Project.vue';
	import Footer from '@/components/Footer.vue';
	export default {
		components: {
			LogoAnimation,
			About,
			Intro,
			Experience,
			Project,
			Footer,
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
	}

	.logo-container {
		color: #fff;
		font-size: 4rem;
	}

	.content-container {
		font-size: 3rem;
		color: var(--text-color1);
	}
</style>
