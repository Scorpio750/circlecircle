<script>
	import Router from './routes/index.svelte';
</script>

<Router />

<style>
	@font-face {
		font-family: "Domaine Display";
		src: local("./fonts/Test Domaine Display/test-domaine-display.woff2") format("woff2");
	}
	:global(body) {
		padding: 0;
		font-family: "Domaine Display", Georgia;
	}
</style>
