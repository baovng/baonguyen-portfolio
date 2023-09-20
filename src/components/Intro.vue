<template>
	<div class="container-fluid vh-100 m-auto">
		<div class="d-flex align-items-start flex-column justify-content-center mx-5 vh-100">
			<h6 class="big-heading bh1 mb-3 show1">{{ h1 }}</h6>
			<h1 class="big-heading bh2 show2">{{ h2 }}</h1>
			<h1 class="big-heading bh2 show3">{{ h3 }}</h1>
			<h6 class="mt-3 big-heading bh3 bh4 show4">
				I am a senior majoring in computer information technology and web developer at
				<span style="color: var(--primary-color)">Texas Christian University</span>. I am currently
				seeking for a full-time job before I graduate in December 2023!
			</h6>
			<a
				href="/resume.pdf"
				target="_blank"
				rel="noopener noreferrer"
				class="btn btn-lg btn-custom mt-4 px-4 text-uppercase show4"
				>See my Resume</a
			>
		</div>
	</div>
</template>

<script>
	export default {
		data() {
			return {
				h1: 'Hi, my name is',
				h2: 'Bao Nguyen.',
				h3: 'I build things for website.',
			};
		},
	};
</script>

<style>
	.big-heading {
		font-family: 'Be Vietnam Pro', serif;
		text-align: left;
	}
	.bh1 {
		color: var(--primary-color);
	}
	.bh2 {
		font-size: 4rem;
		line-height: 5rem;
		font-weight: 900;
	}
	.bh3 {
		font-family: 'Roboto', serif;
		line-height: 2rem;
		font-size: 1rem;
	}
	.bh4 {
		width: 63%;
	}
	.btn-custom {
		border-radius: 0;
		font-size: 1rem;
		color: var(--primary-color);
		border-color: var(--primary-color);
	}
	.btn-custom:hover {
		background-color: var(--background-color);
		color: var(--primary-color);
	}

	.btn:focus {
		box-shadow: none;
	}
	.show1 {
		animation: fade-up 1s ease-in-out;
	}
	.show2 {
		animation: fade-up 1s ease-in-out;
	}
	.show3 {
		animation: fade-up 1.2s ease-in-out;
	}
	.show4 {
		animation: fade-up 1.5s ease-in-out;
	}

	/* Define animations */
	@keyframes fade-up {
		from {
			transform: translateX(-50px);
			opacity: 0;
		}
		to {
			transform: translateX(0px);
			opacity: 1;
		}
	}
</style>
