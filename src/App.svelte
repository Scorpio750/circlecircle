<script>
	import Portfolio from './Portfolio.svelte';
	import SocialLinks from './SocialLinks.svelte';
	import Description from './Description.svelte';
</script>

<header>
	<h1>circlecircle.studio</h1>
</header>
<main>
	<section id="left-half">
		<Portfolio />
		<SocialLinks />
	</section>
	<section id="right-half">
		<Description />
	</section>
</main>
<footer>
	<span>Built by <a href="https://syncretik.co">[Syncretik]</a> 2024, All Rights Reserved.</span>
</footer>

<style>
	:global(body) {
		padding: 0 20vw;
		background-color: #FFF4BE;
	}
	.circle {
		position: absolute;
		border: yellow 50px ridge;
		border-radius: 100%;
		width: 30vw;
		height: 30vw;
		z-index: -10;
		animation: bo 2s infinite linear alternate;
	}

 main {
	 display: flex;
	 flex-flow: row;
	 align-items: space-between;
	}

	#right-Half {
		display: flex;

	}

  footer {
		flex: 1 0 10%;
		opacity: 1;
		background-color: black;
		padding: 1rem;
		font-weight: 900;
		display: flex;
		justify-content: space-between;
	}

	footer a {
		padding: 0 5px;
		text-decoration: none;
		background-color: inherit;
		color: dimgrey;
	}

	footer a:hover {
		color: grey;
	}

	@media (max-width: 768px) {
		:global(body) {
			padding: 0 10vw;
		}
		main {
			display: block;
			height: 100vh;
			font-size: 0.8rem;
		}
	}

</style>
