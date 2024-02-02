<script>
	import Carousel from 'svelte-carousel';
	import Image from './components/Image.svelte';

	const portfolioLinks = new Array(13).fill('').map((_, idx) => {
    const offset = idx + 3;
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
			particlesToShow={3}
			particlesToScroll={2}
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
	@media (max-width: 768px) {
		#carousel {
			max-width: 100vw;
		}
	}
</style>
