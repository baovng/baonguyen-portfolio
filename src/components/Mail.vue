<template>
	<div class="mail-container">
		<div class="mail-content">
			<a href="https://github.com/dacinve" target="_blank">bao.v.nguyen@tcu.edu</a>
		</div>

		<div class="vertical-line"></div>
	</div>
</template>

<script>
	export default {
		data() {
			return {
				email: 'bao.v.nguyen@tcu.edu',
			};
		},
	};
</script>

<style>
	.mail-container {
		position: fixed;
		bottom: 0;
		display: flex;
		flex-direction: column;
		right: 4%;
	}
	.mail-content {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		writing-mode: vertical-rl;
		text-align: center;
		transform: translate(2px, -5px);
	}

	.mail-content a {
		color: #fff;
		font-size: 0.85rem;
		font-family: 'Be Vietnam Pro';
		text-decoration: none;
		letter-spacing: 0.5px;
		transition: all 0.2s ease-in-out;
	}

	.mail-content a:hover {
		transform: translateY(-3px);
		color: var(--primary-color);
	}
</style>
