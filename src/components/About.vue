<template>
	<div class="container-fluid wrapper my-5">
		<div class="d-flex align-items-start flex-column justify-content-center mx-5">
			<div class="header my-5">About Me</div>
			<div class="container mt-3 mb-5">
				<div class="row">
					<div class="col-8 bh3 text-start pe-5">
						<h6 class="big-heading bh3" v-html="me1"></h6>
						<h6 class="big-heading bh3" v-html="me2"></h6>
						<h6 class="big-heading bh3" v-html="me3"></h6>
						<h6 class="big-heading bh3 mt-4" v-html="me4"></h6>
						<div class="row row-cols-2 bh4">
							<div
								class="bh3 col"
								v-for="(lang, index) in langs"
								:key="index"
								style="color: var(--primary-color)"
							>
								<i class="fa fa-light fa-caret-right" />
								{{ lang }}
							</div>
						</div>
					</div>
					<div class="col-4">
						<div class="d-flex justify-content-center align-items center">
							<img src="@/assets/profile.jpeg" alt="profile picture" class="img-fluid" />
						</div>
					</div>
				</div>
			</div>
		</div>
	</div>
</template>
<script>
	export default {
		name: 'About',
		data() {
			return {
				me1: 'My name is Bao Nguyen, I really enjoy creating things that on the internet. My interest in web development since I first took class of Web Designer back in May 2018.',
				me2: "I enjoy being the bridge between <span style='color: var(--primary-color);'>engineering</span> and <span style='color: var(--primary-color);'>design</span>, and feel right as home as a front end engineer. I'm experienced in developing products for the web, from simple landing pages to full-fledged web apps.",
				me3: "Now that I am <span style='color: var(--primary-color);'>seeking a full-time job</span>, I am eager to apply my skills and knowledge to contribute to a dynamic team and take on new challenges in the field of web development.",
				me4: "<span style='color: var(--primary-color);'>Here are a few technologies I've been working with recently:</span>",
				langs: ['JavaScript', 'Vue 3', 'Java', 'SpringBoots', 'MongoDB', 'Python'],
			};
		},
	};
</script>
<style>
	.wrapper {
		width: 100%;
		max-width: 1080px;
	}

	h1 {
		color: var(--text-color1);
		font-size: 2rem;
	}
	.header {
		position: relative;
		font-size: 1.75rem;
		color: var(--primary-color);
		font-weight: 700;
		font-family: 'Roboto';
	}

	.header::before {
		content: '01.  ';
		left: 0;
		font-size: 1.5rem;
		color: var(--primary-color);
	}

	.header::after {
		content: '';
		display: block;
		width: 120%;
		height: 1px;
		background-color: rgb(121, 121, 121);
		position: absolute;
		top: 50%;
		left: 105%;
	}
</style>
