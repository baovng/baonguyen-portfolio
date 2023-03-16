<template>
	<div class="container-fluid">
		<nav class="navbar" :class="navbarClasses" :style="{ transform: translateY }">
			<div class="container-fluid navbar-custom">
				<a href="/" class="logo">
					<img src="@/assets/logo1.png" class="float-start" alt="..." style="width: 44px" />
				</a>

				<div
					class="nav-link nav-link-custom-2 d-flex flex-row justify-content-end align-items-center"
				>
					<div v-for="(section, index) in sections" :key="index" class="ms-4">
						<a :href="'#' + section.id" class="nav-text-custom">
							<span>{{ section.id }} .</span>
							{{ section.section }}
						</a>
					</div>
					<a
						href="/resume.pdf"
						target="_blank"
						rel="noopener noreferrer"
						class="btn btn-sm btn-custom ms-4 px-3 btn-nav"
						>Resume</a
					>
				</div>

				<!-- //toggle menu -->
				<div :class="{ burger: true, toggled: isToggled }">
					<button
						class="toggle-btn"
						@click="isToggled = !isToggled"
						data-bs-toggle="offcanvas"
						data-bs-target="#offcanvasRight"
						aria-controls="offcanvasRight"
					>
						<div :class="{ line: true, 'line-1': true, toggled: isToggled }"></div>
						<div :class="{ line: true, 'line-2': true, toggled: isToggled }"></div>
						<div :class="{ line: true, 'line-3': true, toggled: isToggled }"></div>
					</button>
				</div>
			</div>
		</nav>
		<div
			class="offcanvas offcanvas-end bg-dark"
			id="offcanvasRight"
			aria-labelledby="offcanvasRightLabel"
		>
			<div class="offcanvas-header m-4">
				<div :class="{ burger: true, toggled: isToggled }">
					<button
						class="toggle-btn align-items-center"
						@click="isToggled = !isToggled"
						data-bs-dismiss="offcanvas"
						aria-label="Close"
					>
						<div :class="{ line: true, 'line-1': true, toggled: isToggled }"></div>
						<div :class="{ line: true, 'line-2': true, toggled: isToggled }"></div>
						<div :class="{ line: true, 'line-3': true, toggled: isToggled }"></div>
					</button>
				</div>
			</div>
			<div class="offcanvas-body">
				<div v-for="(section, index) in sections" :key="index">
					<a :href="'#' + section.id" class="nav-text-custom canvas-nav">
						<span>{{ section.id }}.</span>
						{{ section.section }}
					</a>
				</div>
				<a
					href="/resume.pdf"
					target="_blank"
					rel="noopener noreferrer"
					class="btn btn-sm btn-custom mt-5 px-5 btn-nav"
					>Resume</a
				>
			</div>
		</div>
	</div>
</template>

<script>
	export default {
		data() {
			return {
				isHidden: false,
				isFixed: false,
				prevScrollPosition: window.pageYOffset,
				sections: [
					{ id: '01', section: 'About' },
					{ id: '02', section: 'Experiences' },
					{ id: '03', section: 'Project' },
					{ id: '04', section: 'Contact' },
				],
				isToggled: false,
			};
		},
		mounted() {
			window.addEventListener('scroll', this.handleScroll);
		},
		beforeUnmount() {
			window.removeEventListener('scroll', this.handleScroll);
		},
		methods: {
			handleScroll() {
				const currentPosition = window.pageYOffset;

				const scrollDirection = currentPosition > this.prevScrollPosition ? 'down' : 'up';

				if (scrollDirection === 'down') {
					//scroll down, hide navbar after delay
					this.isHidden = true;
					this.isFixed = false;
				} else {
					//scroll up, show navbar
					this.isHidden = false;
					if (currentPosition < window.innerHeight * 0.2) {
						this.isFixed = false;
					} else {
						this.isFixed = true;
					}
				}
				this.prevScrollPosition = currentPosition;
			},
		},
		computed: {
			navbarClasses() {
				return {
					'navbar-hidden': this.isHidden,
					'box-shadow': this.isFixed && !this.isHidden,
				};
			},
			translateY() {
				return `translateY(${this.isHidden ? '-100%' : 0})`;
			},
		},
	};
</script>

<style>
	.navbar {
		width: 100%;
		background: none;
		background-color: rgba(30, 30, 30);
		position: fixed;
		top: 0;
		-webkit-backdrop-filter: blur(10px);
		backdrop-filter: blur(4px);
		border: none;
		transition: transform 0.38s ease-in-out;
		z-index: 10;
		box-shadow: none;
		left: 0;
		padding: 20px 0;
	}
	.navbar-custom {
		margin: 0 2%;
	}
	.navbar-hidden {
		transform: translateY(-100%);
		box-shadow: none;
	}
	.box-shadow {
		box-shadow: 0 2px 10px rgba(20, 20, 20, 0.8);
		background-color: rgba(30, 30, 30, 0.1);
	}
	.nav-link-custom-2 {
		font-size: 0.95rem;
		font-family: 'Rubik', serif;
	}
	.nav-text-custom {
		color: var(--text-color1);
		text-decoration: none;
	}
	.nav-text-custom:hover {
		color: var(--primary-color);
	}
	.nav-text-custom > span {
		color: var(--primary-color);
	}

	.logo {
		transition: all 0.3s ease-in-out;
	}
	.logo:hover {
		transform: scale(1.1);
	}
	.btn-nav {
		font-size: 0.9rem !important;
		font-family: 'Be Vietnam Pro', sans-serif;
		border-radius: 3px !important;
	}
	.offcanvas-header {
		height: 30px;
	}
	.offcanvas-body {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		max-height: 70%;
	}
	.canvas-nav {
		font-size: 1.5rem;
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		margin: 20px 0;
	}
	.toggle-btn {
		background: transparent;
		border: none;
	}
	.burger {
		font-size: 2rem !important;
		font-size: 0rem !important;
		transition: all 0.3s ease-in;
		display: none;
		z-index: 1000;
		/* border: red 1px solid; */
	}
	.burger:hover {
		/* transform: scale(1.1); */
	}
	.line {
		height: 2px;
		width: 30px;
		background-color: var(--primary-color);
	}

	.line-1 {
		margin-bottom: 7px;
		transition: all 0.4s ease-in;
	}
	.line-2 {
		margin-bottom: 7px;
		transition: all 0.4s ease-in;
	}
	.line-3 {
		margin-bottom: 0px;
		transition: all 0.4s ease-in;
	}
	.burger.toggled {
		transform: rotate(180deg);
	}
	.line-1.toggled {
		margin-bottom: -2px;
		transform: rotate(45deg);
	}
	.line-2.toggled {
		margin-bottom: -2px;
		transform: rotate(45deg);
		opacity: 0;
	}
	.line-3.toggled {
		transform: rotate(-45deg);
	}
</style>
