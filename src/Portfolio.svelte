<script>
	import Carousel from 'svelte-carousel';
	import Image from './components/Image.svelte';
</script>

<section class="hero">
	<div id="carousel">
		<Carousel
			autoplay
			autoplayDuration={5000}
			arrows={false}
			particlesToShow={1}
			particlesToScroll={2}
		>
			<Image src="./assets/Betty/A Cloudy Day by the Sea.jpeg" />
			<Image src="./assets/Betty/Cactus Dance II.jpeg" />
			<Image src="./assets/Betty/Cactus Dance.jpeg" />
		</Carousel>
	</div>
</section>

