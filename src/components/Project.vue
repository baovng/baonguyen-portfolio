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
						<h2 style="color: var(--primary-color)" class="">
							<i class="far fa-folder"></i>
						</h2>
						<a :href="project.githubLink" target="_blank" class="d-flex align-items-center">
							<i class="fab fa-github"></i>
						</a>
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
						githubLink: 'https://github.com/CLP-2-0',
						projectName: 'Chinese Learning Platform',
						description:
							'Built a school system that involve different user roles with varying permissions.The website also requires a user authentication system to ensure that only authorized users can access the appropriate pages. ',
						programming: 'Vue 3 / SpringBoots / Auth0 / MongoDB',
					},
					{
						title: '311 Studios',
						githubLink: 'https://github.com/dacinve/311studio',
						projectName: '311 Studios',
						description:
							'A landing page for studio that I built when I first took Web Design. I leaned a lot from this project and land me a decent skill at design',
						programming: 'HTML / CSS / JS',
					},
					{
						title: 'CRUD',
						githubLink: 'https://github.com/dacinve/UserCRUD',
						projectName: 'User CRUD',
						description:
							'My first Vue project of building a web application with CRUD functionality involved creating a system that allows users to Create, Read, Update, and Delete data in a database.',
						programming: 'Vue 3 / Vite / Json DB',
					},
					{
						title: 'TCU',
						githubLink: 'https://github.com/dacinve/WebProject/tree/heroku',
						projectName: 'TCU Horned Frog',
						description:
							'I worked with a team of 4 members, built a full-stack web application for scheduling a Horned Frog TCU for any event. This was my great time that I set a foot on Back-end and Database',
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
				window.open('https://github.com/dacinve?tab=repositories', '_blank');
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
	.card-header > a {
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
