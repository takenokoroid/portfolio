<script>
	import { onMount } from 'svelte';

	let rotationX = 0;
	let rotationY = 0;

	onMount(() => {
		const updateRotation = () => {
			const scrollY = window.pageYOffset;
			rotationX = (scrollY * 360) / window.innerHeight;
			rotationY = (scrollY * 360) / window.innerWidth;
		};

		window.addEventListener('scroll', updateRotation);

		return () => {
			window.removeEventListener('scroll', updateRotation);
		};
	});
</script>

<div class="ball" style="transform: rotateX({rotationX}deg) rotateY({rotationY}deg);" />

<style>
	.ball {
		width: 100px;
		height: 100px;
		background-color: blue;
		border-radius: 50%;
		position: fixed;
		top: 50%;
		left: 50%;
		transform-style: preserve-3d;
	}
</style>
