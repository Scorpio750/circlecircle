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
	main {
		display: grid;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
		z-index: 100;
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
		top: 0;
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
