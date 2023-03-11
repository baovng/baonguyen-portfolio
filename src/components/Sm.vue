<template>
	<div class="social-icons-container">
		<div class="social-icons">
			<a href="https://github.com/dacinve" target="_blank">
				<i class="fab fa-github"></i>
			</a>
			<a href="https://www.linkedin.com/in/bao-nguyen-a08581265/" target="_blank">
				<i class="fab fa-linkedin-in"></i>
			</a>
			<a href="https://www.facebook.com/profile.php?id=100005196251122" target="_blank">
				<i class="fab fa-facebook-f"></i>
			</a>
			<a href="https://www.instagram.com/baovnguyenx/?next=%2F" target="_blank">
				<i class="fab fa-instagram"></i>
			</a>
		</div>

		<div class="vertical-line mt-2"></div>
	</div>
</template>

<style>
	.social-icons-container {
		position: fixed;
		bottom: 0;
		display: flex;
		flex-direction: column;
		left: 4%;
	}

	.vertical-line {
		width: 1px;
		height: 100px;
		background-color: #fff;
		opacity: 0.5;
		margin: 0 auto;
	}

	.social-icons {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
	}

	.social-icons a {
		color: #fff;
		font-size: 20px;
		margin: 5px 0;
		transition: all 0.2s ease-in-out;
	}

	.social-icons a:hover {
		transform: scale(1.2);
		color: var(--primary-color);
	}
</style>
