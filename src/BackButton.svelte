<script>
	import { Link } from 'svelte-routing';
</script>

<Link to="/"><button id="back-btn">Back</button></Link>

<style>
	#back-btn {
		position: absolute;
		left: 3vh;
		top: 1vh;
		font-size: 18px;
		font-family: sans-serif;
		cursor: pointer;
	}
</style>
