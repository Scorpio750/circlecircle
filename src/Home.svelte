<script>
	import Navbar from './Navbar.svelte';
	import Portfolio from './Portfolio.svelte';
	import Description from './Description.svelte';
</script>

<header>
	<h1>circlecircle.studio</h1>
</header>
<main>
	<Navbar />
	<Portfolio />
	<Description />
</main>
<footer>
	Built by <a href="https://syncretik.co">[Syncretik]</a> 2024, All Rights Reserved.
</footer>

<style>
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
	 flex-flow: column;
	 align-items: space-between;
	 background-color: #FFF4BE;
	}

  footer {
		flex: 1 0 10%;
		opacity: 1;
		background-color: black;
		padding: 1rem;
		font-weight: 900;
		display: flex;
		justify-content: flex-end;
		font-family: Verdana;
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
		main {
			display: block;
			height: 100vh;
			font-size: 0.8rem;
		}

		#horizontal-spacer {
			width: 40vw;
			background-color: yellow;
		}
	}

</style>
