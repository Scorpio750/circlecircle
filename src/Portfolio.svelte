<script>
	import Carousel from 'svelte-carousel';
	import Image from './components/Image.svelte';

	const portfolioLinks = new Array(12).fill('').map((_, idx) => {
    const offset = idx;
    const baseIdx = String(offset).padStart(3, '0');
    const baseUrl = './assets/Portfolio/signal-2024-02-01-171154_';
    return baseUrl + baseIdx + '.jpeg';
	});
</script>

<section class="hero">
	<div id="carousel">
		<Carousel
			autoplay
			autoplayDuration={5000}
			arrows={false}
			particlesToShow={1}
			particlesToScroll={1}
		>
			{#each portfolioLinks as link}
				<Image src={link} />
			{/each}
		</Carousel>
	</div>
</section>

<style>
	#carousel {
		max-width: 29vw;
		box-shadow: -16px 10px 10px goldenrod;
	}
	@media (max-width: 999px) {
		#carousel {
			max-width: 100%;
		}
	}
</style>
