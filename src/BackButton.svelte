<script>
	import { Link } from 'svelte-routing';
</script>

<Link to="/"><button id="back-btn">&larr</button></Link>

<style>
	#back-btn {
		position: absolute;
		left: 0;
		top: 50vh;
		font-size: 54px;
		font-family: sans-serif;
		cursor: pointer;
	}
</style>
