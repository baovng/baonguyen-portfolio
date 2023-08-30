<template>
	<div class="container-fluid vh-65">
		<div class="d-flex align-items-start flex-column justify-content-center mx-5">
			<div class="header header-2 my-5">Experiences</div>
			<div class="container mt-4 bh3 fixed-width">
				<div class="d-flex align-items-start vertical">
					<div
						class="nav flex-column nav-pills me-3"
						id="v-pills-tab"
						role="tablist"
						aria-orientation="vertical"
					>
						<button
							class="nav-link nav-link-custom active"
							id="v-pills-intern-tab"
							data-bs-toggle="pill"
							data-bs-target="#v-pills-intern"
							type="button"
							role="tab"
							aria-controls="v-pills-intern"
							aria-selected="true"
						>
							FinThrive
						</button>
						<button
							class="nav-link nav-link-custom"
							id="v-pills-home-tab"
							data-bs-toggle="pill"
							data-bs-target="#v-pills-home"
							type="button"
							role="tab"
							aria-controls="v-pills-home"
							aria-selected="true"
						>
							TCU
						</button>
						<button
							class="nav-link nav-link-custom"
							id="v-pills-profile-tab"
							data-bs-toggle="pill"
							data-bs-target="#v-pills-profile"
							type="button"
							role="tab"
							aria-controls="v-pills-profile"
							aria-selected="false"
						>
							TCU
						</button>
						<button
							class="nav-link nav-link-custom"
							id="v-pills-messages-tab"
							data-bs-toggle="pill"
							data-bs-target="#v-pills-messages"
							type="button"
							role="tab"
							aria-controls="v-pills-messages"
							aria-selected="false"
						>
							Freelance
						</button>
						<button
							class="nav-link nav-link-custom"
							id="v-pills-settings-tab"
							data-bs-toggle="pill"
							data-bs-target="#v-pills-settings"
							type="button"
							role="tab"
							aria-controls="v-pills-settings"
							aria-selected="false"
						>
							Start up
						</button>
					</div>
					<div class="tab-content" id="v-pills-tabContent">
						<div
							class="tab-pane fade show active"
							id="v-pills-intern"
							role="tabpanel"
							aria-labelledby="v-pills-intern-tab"
						>
							<h5 class="bh1 text-start">{{ job5des }}</h5>
							<h6 class="bh5 mt-2 mb-3">{{ job5Time }}</h6>
							<h6 class="bh5 lh-base mx-3" v-for="(job, index) in job5" :key="index">
								<i class="fa fa-light fa-caret-right me-2" />
								{{ job }}
							</h6>
						</div>
						<div
							class="tab-pane fade show"
							id="v-pills-home"
							role="tabpanel"
							aria-labelledby="v-pills-home-tab"
						>
							<h5 class="bh1 text-start">{{ job1des }}</h5>
							<h6 class="bh5 mt-2 mb-3">{{ job1Time }}</h6>
							<h6 class="bh5 lh-base mx-3" v-for="(job, index) in job1" :key="index">
								<i class="fa fa-light fa-caret-right me-2" />
								{{ job }}
							</h6>
						</div>
						<div
							class="tab-pane fade"
							id="v-pills-profile"
							role="tabpanel"
							aria-labelledby="v-pills-profile-tab"
						>
							<h5 class="bh1 text-start">{{ job2des }}</h5>
							<h6 class="bh5 mt-2 mb-3">{{ job2Time }}</h6>
							<h6 class="bh5 lh-base mx-3" v-for="(job, index) in job2" :key="index">
								<i class="fa fa-light fa-caret-right me-2" />
								{{ job }}
							</h6>
						</div>
						<div
							class="tab-pane fade"
							id="v-pills-messages"
							role="tabpanel"
							aria-labelledby="v-pills-messages-tab"
						>
							<h5 class="bh1 text-start">{{ job3des }}</h5>
							<h6 class="bh5 mt-2 mb-3">{{ job3Time }}</h6>
							<h6 class="bh5 lh-base mx-3" v-for="(job, index) in job3" :key="index">
								<i class="fa fa-light fa-caret-right me-2" />
								{{ job }}
							</h6>
						</div>
						<div
							class="tab-pane fade"
							id="v-pills-settings"
							role="tabpanel"
							aria-labelledby="v-pills-settings-tab"
						>
							<h5 class="bh1 text-start">{{ job4des }}</h5>
							<h6 class="bh5 mt-2 mb-3">{{ job4Time }}</h6>
							<h6 class="bh5 lh-base mx-3" v-for="(job, index) in job4" :key="index">
								<i class="fa fa-light fa-caret-right me-2" />
								{{ job }}
							</h6>
						</div>
					</div>
				</div>
				<!-- this is for horizontal -->
				<div class="horizontal">
					<nav class="horizontal-scroll">
						<div class="nav nav-pills my-3" id="nav-tab" role="tablist">
							<button
								class="nav-link active nav-link-custom-horizontal"
								id="nav-5-tab"
								data-bs-toggle="tab"
								data-bs-target="#nav-5"
								type="button"
								role="tab"
								aria-controls="nav-5"
								aria-selected="true"
							>
								FinThrive
							</button>
							<button
								class="nav-link nav-link-custom-horizontal"
								id="nav-1-tab"
								data-bs-toggle="tab"
								data-bs-target="#nav-1"
								type="button"
								role="tab"
								aria-controls="nav-1"
								aria-selected="true"
							>
								TCU
							</button>
							<button
								class="nav-link nav-link-custom-horizontal"
								id="nav-2-tab"
								data-bs-toggle="tab"
								data-bs-target="#nav-2"
								type="button"
								role="tab"
								aria-controls="nav-2"
								aria-selected="false"
							>
								TCU
							</button>
							<button
								class="nav-link nav-link-custom-horizontal"
								id="nav-3-tab"
								data-bs-toggle="tab"
								data-bs-target="#nav-3"
								type="button"
								role="tab"
								aria-controls="nav-3"
								aria-selected="false"
							>
								Freelance
							</button>
							<button
								class="nav-link nav-link-custom-horizontal"
								id="nav-4-tab"
								data-bs-toggle="tab"
								data-bs-target="#nav-4"
								type="button"
								role="tab"
								aria-controls="nav-4"
								aria-selected="false"
							>
								Start up
							</button>
						</div>
					</nav>

					<div class="tab-content" id="nav-tabContent">
						<div
							class="tab-pane fade show active mx-3"
							id="nav-5"
							role="tabpanel"
							aria-labelledby="nav-5-tab"
						>
							<h5 class="bh1 text-start">{{ job5des }}</h5>
							<h6 class="bh5 mt-2 mb-3">{{ job5Time }}</h6>
							<h6 class="bh5 lh-base mx-3" v-for="(job, index) in job5" :key="index">
								<i class="fa fa-light fa-caret-right me-2" />
								{{ job }}
							</h6>
						</div>
						<div
							class="tab-pane fade show mx-3"
							id="nav-1"
							role="tabpanel"
							aria-labelledby="nav-1-tab"
						>
							<h5 class="bh1 text-start">{{ job1des }}</h5>
							<h6 class="bh5 mt-2 mb-3">{{ job1Time }}</h6>
							<h6 class="bh5 lh-base mx-3" v-for="(job, index) in job1" :key="index">
								<i class="fa fa-light fa-caret-right me-2" />
								{{ job }}
							</h6>
						</div>
						<div class="tab-pane fade mx-3" id="nav-2" role="tabpanel" aria-labelledby="nav-2-tab">
							<h5 class="bh1 text-start">{{ job2des }}</h5>
							<h6 class="bh5 mt-2 mb-3">{{ job2Time }}</h6>
							<h6 class="bh5 lh-base mx-3" v-for="(job, index) in job2" :key="index">
								<i class="fa fa-light fa-caret-right me-2" />
								{{ job }}
							</h6>
						</div>
						<div class="tab-pane fade mx-3" id="nav-3" role="tabpanel" aria-labelledby="nav-3-tab">
							<h5 class="bh1 text-start">{{ job3des }}</h5>
							<h6 class="bh5 mt-2 mb-3">{{ job3Time }}</h6>
							<h6 class="bh5 lh-base mx-3" v-for="(job, index) in job3" :key="index">
								<i class="fa fa-light fa-caret-right me-2" />
								{{ job }}
							</h6>
						</div>
						<div class="tab-pane fade mx-3" id="nav-4" role="tabpanel" aria-labelledby="nav-4-tab">
							<h5 class="bh1 text-start">{{ job4des }}</h5>
							<h6 class="bh5 mt-2 mb-3">{{ job4Time }}</h6>
							<h6 class="bh5 lh-base mx-3" v-for="(job, index) in job4" :key="index">
								<i class="fa fa-light fa-caret-right me-2" />
								{{ job }}
							</h6>
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
				job1des: 'Chinese Learning Platform Development',
				job1: [
					'Develop frontend and backend for the engaging learning platform for TCU students using VueJS, SpringBoots, and MongoDB',
					'Architect robust core features: course management, user profiles and management, assignment submissions, and grades tracking',
					'Implement responsive web design principles on mobile devices to increase platform traffic by 50%',
					'Lead team members on integrating Auth0 as the primary authentication and authorization solution, ensuring secure and streamlined access to user accounts and resources',
					"Conduct rigorous testings and debuggings to ensure the platform's stability, performance, and security",
					'Design a backend of the discussion forum page to reduce platform refreshing time by 70% and boost user interactions',
				],
				job1Time: 'Aug 2022 - May 2023',

				job2des: 'Java and Python-based system help desk',
				job2: [
					'Resolved Java and Python related technical issues and coding bugs on students’ programming projects, increasing customer satisfaction rate to 95%',
					'Utilized knowledge of Java, Python, and MongoDB to troubleshoot and resolve a range of issues',
					'Documented the standard operating procedures for team members to troubleshoot similar issues, reducing tickets cycle time by 50%',
					'Provided guidance to students to improving the performance and user satisfaction',
				],
				job2Time: 'Jan 2022 - May 2022',

				job3des: 'Freelance Web Developer',
				job3: [
					'Designed mobile version and custom websites for nails salon featuring service menu and monthly promotions',
					'Developed the dynamic pricing feature to estimate service costs based on customer selections, achieving in 60% business traffic increase',
					'Integrated the seamlessly language switching to server Spanish speaking customers, increasing local customers by 30%',
					'Incorporated customer feedbacks to enhance website and update contents and increase customer loyalty',
					'Regularly maintained websites to remain website availability at 99%',
				],
				job3Time: 'May 2018 - Jan 2021',

				job4des: 'E-commerce Product Specialist',
				job4: [
					'Established an e-commerce platform to sell products online and conducted market research to identify customer needs and preferences',
					'Analyzed sales data and customer feedback to identify trends and optimize product offerings, increasing 25% sale volume',
					'Facilitated the procurement of inventory and ensured customers had access to up-to-date delivery information',
					'Implemented email marking campagins, resulted in 30% increase in returning customers and 20% customer referrals',
				],
				job4Time: 'July 2018 - Aug 2019',

				job5des: 'Web Developer Intern',
				job5: [
					"Collaborated cross-functional team to implement rebranding initiative with the FinThrive's new identity using Angular",
					'Successfully upgraded Angular and Angular Material from v10 to v16 for three primary CDM products at FinThrive',
					"Researched and comprehensively documented Angular upgrade guidelines for the team's future endeavors ",
					"Developed and integrated new feature, ‘Save View on Filter', from debugging to testing, resulting in an optimized user workflow, and enabling customized data views",
					'Actively participated in Agile methodologies, engaging in daily stand-ups, contributing to sprint planning, mastering task tracking and management using Jira',
					'Utilized Azure DevOps for version control, continuous integration, and project management',
				],
				job5Time: 'Jun 2023 - Aug 2023',
			};
		},
	};
</script>
<style>
	.horizontal {
		display: none;
	}
	.vh-65 {
		min-height: 60vh;
		height: auto;
	}
	.fixed-width {
		max-width: 750px;
	}
	h1 {
		color: var(--text-color1);
		font-size: 2rem;
	}
	.bh5 {
		color: var(--text-color2);
		text-align: left;
	}

	.header-2::before {
		content: '02.  ';
		left: 0;
		margin-right: 10px;
		font-size: 1.5rem;
		color: var(--primary-color);
	}

	/* active nav link */
	.nav-link-custom {
		color: var(--text-color1);
		text-align: left;
		padding: 5px 20px;
		border-left: 2px solid var(--decor-color) !important ;
		border-radius: 0 !important ;
		transition: border-left 0.5s ease-in-out;
		font-size: 0.9rem;
	}

	.nav-pills .nav-link-custom.active {
		background-color: var(--background-color) !important;
		color: var(--primary-color);
		border-left: 2px solid var(--primary-color) !important;
		border-radius: 0;
	}

	/* hover state */
	.nav-pills .nav-link-custom:hover {
		background-color: var(--background-color);
		color: var(--primary-color);
	}
	.nav-pills .nav-link-custom.active ~ .nav-link-custom {
		transition: border-left 0.5s ease-in-out;
	}

	.nav-pills .nav-link-custom.active ~ .nav-link-custom:hover {
		background-color: var(--background-color);
		color: var(--primary-color);
		border-left-color: var(--primary-color) !important;
	}
	/* For horizontal */

	.nav-link-custom-horizontal {
		color: var(--text-color1);
		text-align: left;
		padding: 5px 30px;
		border-bottom: 2px solid var(--decor-color) !important ;
		border-radius: 0 !important ;
		transition: border-left 0.5s ease-in-out;
		font-size: 0.9rem;
	}
	.nav-pills .nav-link-custom-horizontal.active {
		background-color: var(--background-color) !important;
		color: var(--primary-color);
		border-bottom: 2px solid var(--primary-color) !important;
		border-radius: 0;
	}

	.nav-pills .nav-link-custom-horizontal:hover {
		background-color: var(--background-color);
		color: var(--primary-color);
	}
	.nav-pills .nav-link-custom-horizontal.active ~ .nav-link-custom-horizontal {
		transition: border-left 0.5s ease-in-out;
	}

	.nav-pills .nav-link-custom-horizontal.active ~ .nav-link-custom-horizontal:hover {
		background-color: var(--background-color);
		color: var(--primary-color);
		border-bottom-color: var(--primary-color) !important;
	}

	.horizontal-scroll {
		overflow-x: auto;
	}
	.horizontal-scroll > .nav {
		flex-wrap: nowrap;
	}
</style>
