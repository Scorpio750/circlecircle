<script>
	import Router from './routes/index.svelte';
	export let name;
</script>

<main>
	<Router />
	<div class="circle" id="circle1" />
	<div class="circle" id="circle2" />
</main>
	<footer>
		Built by Syncretik 2021, All Rights Reserved.
	</footer>

<style>
	main {
		margin: 0 auto;
		z-index: 100;
		height: 90vh;
		width: 100vw;
	}

	footer {
		flex-basis: 10%;
		padding: 1rem 0;
		display: flex;
		flex-flow: row nowrap;
		justify-content: flex-end;
		font-weight: 900;
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
		top: 10vh;
		left: 10vw;
	}

	#circle2 {
		top: 25vh;
		left: 25vw;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>
