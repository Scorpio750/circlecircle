<script>
	import { Link } from 'svelte-routing';
</script>

<main>
	<img src="https://nyc3.digitaloceanspaces.com/circlecircle.studio/mtahearts.jpeg" alt="boobooboo">
<Link to="/"><button>Back</button></Link>
</main>

<style>
	/* :global(body) { */
	/* 	background-color: black; */
	/* } */

	main {
		display: flex;
		flex-flow: column nowrap;
		justify-content: center;
		align-items: center;
	}

	img {

	}
</style>
