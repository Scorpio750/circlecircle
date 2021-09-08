<script>
	import Description from './Description.svelte';
	import Block from './Block.svelte';
</script>

<main>
	<Description />
	<Block />
	<!--div class="circle" id="circle1" />
	<div class="circle" id="circle2" /-->
</main>

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

	#circle1 {
		top: 5vh;
		left: 5vw;
	}

	#circle2 {
		top: 20vh;
		left: 20vw;
	}

	main {
		height: 100vh;
		display: grid;
		grid-template-columns: repeat(8, minmax(10px, 1fr));
		grid-template-rows: repeat(8, minmax(10px, 1fr));
	}

	@media (max-width: 960px) {
		main {
			display: block;
			font-size: 0.8rem;
		}

		#horizontal-spacer {
			width: 40vw;
			background-color: yellow;
		}

		#Block {
			display: none !important;
		}
	}
</style>
