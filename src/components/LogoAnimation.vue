<template>
	<div class="logo-animation">
		<svg width="100" height="100">
			<polygon
				:points="points"
				:stroke="lineColor"
				:stroke-width="lineWidth"
				fill="transparent"
				class="hexagon"
			/>
		</svg>
	</div>
</template>

<script>
	export default {
		data() {
			return {
				// the vertices of hexagon:
				// r is radius
				// (x1, y1) = (r * cos(0), r * sin(0))
				// (x2, y2) = (r * cos(pi/3), r * sin(pi/3))
				// (x3, y3) = (r * cos(2*pi/3), r * sin(2*pi/3))
				// (x4, y4) = (r * cos(pi), r * sin(pi))
				// (x5, y5) = (r * cos(4*pi/3), r * sin(4*pi/3))
				// (x6, y6) = (r * cos(5*pi/3), r * sin(5*pi/3))
				points: '50,0 95,25 95,75 50,100 5,75 5,25',
				lineColor: '#fff',
				lineWidth: 4,
			};
		},
	};
</script>

<style scoped>
	.logo-animation {
		display: flex;
		justify-content: center;
		align-items: center;
	}

	.hexagon {
		stroke-dasharray: 350;
		stroke-dashoffset: 350;
		animation: draw 2s ease forwards;
	}

	@keyframes draw {
		to {
			stroke-dashoffset: 0;
		}
	}
</style>
