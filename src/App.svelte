<script>
	import Router from './routes/index.svelte';
	export let name;
</script>

<main>
	<Router />
	<div class="circle" id="circle1" />
	<div class="circle" id="circle2" />
</main>

<style>
	:global(body) {
		padding: 0;
	}
	main {
		margin: 0 auto;
		z-index: 100;
		height: 100vh;
		width: 100vw;
	}


	.circle {
		position: absolute;
		border: yellow 20px solid;
		border-radius: 100%;
		width: 30vw;
		height: 30vw;
		z-index: -100;
		animation: bo 2s infinite linear alternate;
	}

	#circle1 {
		top: 5vh;
		left: 5vw;
	}

	#circle2 {
		top: 20vh;
		left: 20vw;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>
