<template>
	<div class="container-fluid my-5">
		<div class="d-flex align-items-start flex-column justify-content-center mx-5">
			<div class="header header-3 my-5">What I've build</div>

			<div class="project-grid mb-4 mx-auto">
				<div
					class="project-card"
					v-for="(project, index) in projects"
					:key="index"
					@mouseover="animateCard(index, true)"
					@mouseleave="animateCard(index, false)"
				>
					<div class="card-header">
						<h2 style="color: var(--primary-color)">
							<i class="far fa-folder fs-3"></i>
						</h2>
						<div class="d-flex">
							<a :href="project.githubLink" target="_blank" class="d-flex align-items-center me-3">
								<i class="fab fa-github fs-3"></i>
							</a>
							<a :href="project.link" target="_blank" class="d-flex align-items-center">
								<i class="fa-solid fa-arrow-up-right-from-square"></i>
							</a>
						</div>
					</div>
					<div class="card-body">
						<h5 class="bh1 text-start fw-bold" v-html="project.projectName"></h5>
						<p class="bh5 bh7">{{ project.description }}</p>
					</div>
					<div class="card-footer">
						<p class="bh5 bh8 m-0">{{ project.programming }}</p>
					</div>
				</div>
			</div>
			<button
				class="btn btn-lg btn-custom mt-5 px-4 text-uppercase view-more-btn"
				@click="viewMoreProjects"
				target="_blank"
			>
				View more my project
			</button>
		</div>
	</div>
</template>
<script>
	export default {
		data() {
			return {
				projects: [
					{
						title: 'Chinese Learning Platform',
						link: 'https://chinesetcu.netlify.app',
						githubLink: 'https://github.com/orgs/CLP-2-0/repositories',
						projectName: 'Chinese Learning Platform',
						description:
							'Built a school system that involve different user roles with varying permissions. The website also requires a user authentication system to ensure that only authorized users can access the appropriate pages. ',
						programming: 'Vue 3 / SpringBoots / Auth0 / MongoDB',
					},
					{
						title: 'T & C Nails',
						link: 'https://tcnails.netlify.app',
						githubLink: 'https://github.com/baovng/TCNail',
						projectName: 'TC Nail Salon',
						description:
							'TC Nail Salon is a tailor-made nail salon website crafted to meet the unique needs of our clients. Not only showcases wide range of nail services, but also provides transparent pricing details and exclusive promotional discounts.',
						programming: 'Vue 3 / Bootstraps / JS',
					},
					{
						title: 'QR Generator',
						link: 'https://bv-qrgenerator.netlify.app',
						githubLink: 'https://github.com/baovng/QRGenerator',
						projectName: 'QR Generator',
						description:
							'QR Generator Website: Your one-stop destination for creating customized QR codes effortlessly. Generate QR codes for websites, contact information, promotions, and more, with ease',
						programming: 'HTML / CSS / JS',
					},
					{
						title: '311 Studios',
						link: 'https://311studios.netlify.app/',
						githubLink: 'https://github.com/dacinve/311studio',
						projectName: '311 Studios',
						description:
							'A landing page for studio that I built when I first took Web Design. I leanred a lot from this project and landed me a decent skill at design.',
						programming: 'HTML / CSS / JS',
					},
					{
						title: 'Weather',
						link: 'https://weather-city-search.netlify.app',
						githubLink: 'https://github.com/baovng/weatherapp',
						projectName: 'Weather App',
						description:
							'I created a Weather App based on City, get accurate, up-to-date forecasts and real-time wather data tailored to the location.',
						programming: 'HTML / CSS / JS',
					},
					// {
					// 	title: 'CRUD',
					// 	link: 'https://usercrud111.netlify.app/',
					// 	githubLink: 'https://github.com/dacinve/UserCRUD',
					// 	projectName: 'User CRUD',
					// 	description:
					// 		'My first Vue project of building a web application with CRUD functionality involved creating a system that allows users to Create, Read, Update, and Delete data in a database.',
					// 	programming: 'Vue 3 / Vite / Json DB',
					// },
					{
						title: 'TCU',
						link: 'https://frogproject.netlify.app/',
						githubLink: 'https://github.com/dacinve/WebProject/tree/heroku',
						projectName: 'TCU Horned Frog',
						description:
							'I worked with a team of 4 members to built a full-stack web application for scheduling a TCU Horned Frog mascot for events. The project gave me a decent experiences on the Back-end and Database.',
						programming: 'Vue 3 / SpringBoots / MySQL',
					},
				],
			};
		},
		methods: {
			animateCard(index, isHovered) {
				const card = document.querySelectorAll('.project-card')[index];
				if (isHovered) {
					card.style.transform = 'translateY(-12px)';
				} else {
					card.style.transform = 'translateY(0)';
				}
			},
			viewMoreProjects: function () {
				window.open('https://github.com/baovng', '_blank');
			},
		},
	};
</script>
<style>
	.header-3::before {
		content: '03.  ';
		margin-right: 10px;
	}
	.project-grid {
		display: grid;
		grid-template-columns: repeat(3, 1fr);
		grid-gap: 20px;
	}

	.project-card {
		background-color: var(--background-color);
		padding: 15px 5px;
		height: auto;
		min-height: 350px;
		width: 100%;
		max-width: 300px;
		box-shadow: 5px 5px 20px rgb(19, 19, 19);
		transition: transform 0.2s ease-out;
		display: flex;
		flex-direction: column;
		justify-content: space-between;
		overflow: hidden;
	}

	.card-header {
		display: flex;
		justify-content: space-between;
		align-items: center;
		border: none;
		background: none;
	}
	.card-footer {
		border: none;
		background: none;
	}

	.card-header h2 {
		margin-bottom: 0;
	}

	.card-header h2 i {
		font-size: 30px;
	}
	.card-header a i {
		font-size: 24px;
		color: #555;
		transition: color 0.2s ease-out;
	}

	.card-header a:hover i {
		color: var(--primary-color);
	}
	.card-header a {
		text-decoration: none;
	}

	.card-body h2 {
		margin: 0;
	}

	.card-body p {
		margin: 0;
		margin-bottom: 10px;
		line-height: 1.5;
	}

	.card-body p:last-of-type {
		margin-bottom: 0;
	}
	.bh7 {
		font-size: 1rem;
	}
	.bh8 {
		font-size: 0.8rem;
	}
	.view-more-btn {
		display: block;
		margin: 0 auto;
		text-align: center;
	}
	.btn:visited {
		border-color: none;
	}
</style>
