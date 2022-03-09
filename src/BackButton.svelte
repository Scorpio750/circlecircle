<script>
	import { Link } from 'svelte-routing';
</script>

<Link to="/"><button id="back-btn">&#8617;</button></Link>

<style>
	#back-btn {
		position: absolute;
		left: 0;
		top: 0;
		font-size: 32px;
		cursor: pointer;
	}
</style>
