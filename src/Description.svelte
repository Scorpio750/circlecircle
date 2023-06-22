<script>
	import projects from './projects.js';
	import { link } from 'svelte-routing';
	import Carousel from 'svelte-carousel';
	import Image from './components/Image.svelte';
</script>

<div id="description-section">
		<header>
			<h1>circlecircle.studio</h1>
		</header>
		<div class="text-tile">
			<p>setting up my own website is very time consuming and I'm pretty much exhausted all the time.</p>

			<p>I have better things to do like overshare on
				<a href="https://www.instagram.com/copy____cat___/">Instagram</a>
				 and
				<a href="https://www.facebook.com/facebo/">Facebook</a>
			</p>

			<p>knowing me, this thing will forever be under construction - so i forced this
			<a href="https://syncretik.co">shit-eating goblin</a>
			to make it for me</p>

			<p>for now, check out some stuff I did, or tried to do:</p>
		</div>
		<section class="hero">
			<div id="carousel">
				<Carousel
					autoplay
					autoplayDuration={5000}
					arrows={false}
					particlesToShow={3}
					particlesToScroll={2}
				>
					<Image src="./assets/Betty/A Cloudy Day by the Sea.jpeg" />
					<Image src="./assets/Betty/Cactus Dance II.jpeg" />
					<Image src="./assets/Betty/Cactus Dance.jpeg" />
				</Carousel>
			</div>
		</section>
		<div class="text-tile">
			{#each projects as project}
			<li>
				{#if project.name === "Betty" || project.name === "chananigans"}
				<a href={project.name.toLowerCase()} use:link>{project.name}</a>
				{:else}
				<a target="_blank" href={project.link}>{project.name}</a>
				{/if}
				- {project.description}
			</li>
			{/each}
	</div>
</div>

<style>
	header {
		margin: 1rem 0;
	}

	#description-section {
		margin: 0 2rem;
		display: flex;
		flex-flow: column;
		align-items: center;
		background-image:  repeating-radial-gradient( circle at 0 0, transparent 0, #e5e5f7 100px ), repeating-linear-gradient( yellow, lightyellow );
	}

	.hero {
		display: flex;
		justify-content: center;
	}

	#carousel {
		width: 50vw;
	}

	@media screen and (max-width: 960px) {
		#description-section {
			padding: 1em;
			margin: 0;
		}
	}

	@media screen and (max-width: 640px) {
		#description-section h1 {
			font-size: 1.75rem;
			font-weight: 900;
		}

		.tile-text {
			width: 80vw;
		}
	}

	h1 {
		font-size: 3em;
		font-weight: 100;
	}

	p {
		font-size: 20px;
	}

	li {
		font-size: 18px;
		margin: 10px;
		list-style-type: armenian;
	}

 a {
		padding:3px 5px;
		color: white;
		background-color: black;
		border-radius: 9999px;
		/* animation: glowy 1s alternate infinite ease-out; */
	}

	@keyframes glowy {
		from {
		}

		to {
			color: yellow;
			background-color: white;
		}
	}

	a:hover {
		color: black;
		background-color: white;
	}

	.text-tile {
		background-color: #FFE568;
		width: 50vw;
	}

	#horizontal-spacer {
		margin: 3rem 0;
		width: 10rem;
		height: 2rem;
		background-color: black;
		border-radius: 5px;;
	}

	li:nth-child(2n) {
		list-style: disc;
	}

	li:nth-child(2n+1) {
		list-style: circle;
	}

	@media screen and (max-width: 640px) {
		h1 { font-size: 3rem; line-height: 1.25; }

		a {
			padding: 0 4px;
		}

		#horizontal-spacer {
			width: 85vw;
			background-color: yellow;
			border-radius: 0;
		}

	}
</style>
