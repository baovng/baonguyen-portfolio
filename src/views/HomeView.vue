<template>
	<div class="logo-container vh-100" v-if="showLogo">
		<div class="logo-animation">
			<LogoAnimation />
		</div>
	</div>

	<div class="content-container d-flex flex-column" v-else>
		<Navbar />
		<div class="main">
			<section>
				<Intro />
			</section>
			<section id="01">
				<About />
			</section>
			<section id="02" class="mt-5">
				<Experience />
			</section>
			<section id="03">
				<Project />
			</section>

			<section class="sm">
				<Sm />
			</section>
			<section class="sm">
				<Mail />
			</section>
			<section id="04">
				<Contact />
			</section>
			<section>
				<Footer />
			</section>
		</div>
	</div>
</template>

<script>
	import LogoAnimation from '../components/LogoAnimation.vue';
	import Navbar from '@/components/Navbar.vue';
	import About from '@/components/About.vue';
	import Intro from '@/components/Intro.vue';
	import Experience from '@/components/Experience.vue';
	import Project from '@/components/Project.vue';
	import Footer from '@/components/Footer.vue';
	import Sm from '@/components/Sm.vue';
	import Mail from '@/components/Mail.vue';
	import Contact from '@/components/Contact.vue';
	export default {
		components: {
			LogoAnimation,
			Navbar,
			About,
			Intro,
			Experience,
			Project,
			Footer,
			Sm,
			Mail,
			Contact,
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
	section {
		max-width: 1000px;
		/* background-color: rgb(59, 32, 71); */
	}
</style>
