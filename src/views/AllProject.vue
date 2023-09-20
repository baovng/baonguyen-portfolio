<template>
	<div class="content-container d-flex flex-column">
		<Navbar />
		<div class="testing">
			<table class="mt-5">
				<tr class="test2">
					<td>Testing</td>
				</tr>
				<tr>
					<td>Testing</td>
				</tr>
			</table>
		</div>
	</div>
</template>

<script>
	import Navbar from '@/components/Navbar.vue';

	export default {
		components: {
			Navbar,
		},
	};
</script>

<style>
	.testing {
		margin-top: 30px;
		min-height: 80vh;
		width: 80%;
	}
	.test2 {
		color: #fff;
	}
</style>
