<template>
	<div class="container-fluid">
		<div class="d-flex align-items-start flex-column justify-content-center mx-5">
			<div class="header header-1 my-5">About Me</div>
			<div class="container mt-3 mb-5">
				<div class="row custom-about">
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
				me1: "From as early as I can remember, I have always had a fascination with <span style='color: var(--primary-color);'>computers</span> and the way in which they work. <span style='color: var(--primary-color);'>Computer science</span> is thus, the natural progression for me as I continue to define the person I wanted to become in later life.",
				me2: "I enjoy being the bridge between <span style='color: var(--primary-color);'>engineering</span> and <span style='color: var(--primary-color);'>design</span>, and feel right as home as a front-end engineer. I am experienced in developing products for the web, from simple landing pages to full-fledged web apps.",
				me3: "Now that I am <span style='color: var(--primary-color);'>seeking a full-time job</span>, I am eager to apply my skills and knowledge to contribute to a dynamic team and take on new challenges in the field of web development.",
				me4: "<span style='color: var(--primary-color);'>Here are a few technologies I've been working with recently:</span>",
				langs: [
					'JavaScript',
					'Vue 3',
					'Java',
					'SpringBoots',
					'MongoDB',
					'Python',
					'Angular',
					'Azure DevOps',
				],
			};
		},
	};
</script>
<style>
	h1 {
		color: var(--text-color1);
		font-size: 2rem;
	}
	.header {
		position: relative;
		font-size: 1.5rem;
		color: var(--primary-color);
		font-weight: 700;
		font-family: 'Roboto';
	}

	.header-1::before {
		content: '01.  ';
		left: 0;
		font-size: 1.5rem;
		color: var(--primary-color);
	}

	.header::after {
		content: '';
		display: block;
		width: 100%;
		height: 1px;
		background-color: rgb(121, 121, 121);
		position: absolute;
		top: 50%;
		left: 105%;
	}

	.img-fluid {
		transition: all 0.2s ease-in-out;
		box-shadow: 5px 10px 25px var(--primary-color);
	}
	.img-fluid:hover {
		transform: scale(1.03);
	}
</style>
