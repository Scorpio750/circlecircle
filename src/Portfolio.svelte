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
			particlesToShow={2}
			particlesToScroll={2}
		>
			<Image src="./assets/Betty/A Cloudy Day by the Sea.jpeg" />
			<Image src="./assets/Betty/Cactus Dance II.jpeg" />
			<Image src="./assets/Betty/Cactus Dance.jpeg" />
			<Image src="./assets/Betty/Cloud Garden.jpeg" />
			<Image src="./assets/Betty/Colorcruise.jpeg" />
			<Image src="./assets/Betty/Cosmic Dust.jpeg" />
			<Image src="./assets/Betty/Darkness Creeps In.jpeg" />
			<Image src="./assets/Betty/Deathstar.jpeg" />
			<Image src="./assets/Betty/Discovery.jpeg" />
			<Image src="./assets/Betty/Diver.jpeg" />
			<Image src="./assets/Betty/Everything Dies.jpeg" />
			<Image src="./assets/Betty/Falling Off the Canvas.jpeg" />
			<Image src="./assets/Betty/Flora.jpeg" />
			<Image src="./assets/Betty/Funnel.jpeg" />
			<Image src="./assets/Betty/Jitters.jpeg" />
			<Image src="./assets/Betty/Kestrel.jpeg" />
			<Image src="./assets/Betty/Kineticity.jpeg" />
			<Image src="./assets/Betty/King Frog.jpeg" />
			<Image src="./assets/Betty/Last of the Dinosaurs.jpeg" />
			<Image src="./assets/Betty/Mecharoot.jpeg" />
			<Image src="./assets/Betty/Mesh Potatoes.jpeg" />
			<Image src="./assets/Betty/New Perspective.jpeg" />
			<Image src="./assets/Betty/Roads that Lead to Something.jpeg" />
			<Image src="./assets/Betty/Serpentine.jpeg" />
			<Image src="./assets/Betty/Shirley & the Medium Hypnosis.jpeg" />
			<Image src="./assets/Betty/Space Junk.jpeg" />
			<Image src="./assets/Betty/Tangle.jpeg" />
			<Image src="./assets/Betty/the-end.jpeg" />
			<Image src="./assets/Betty/This Could Be Sexual.jpeg" />
			<Image src="./assets/Betty/Unstructural Sound.jpeg" />
			<Image src="./assets/Betty/Valleys & Peaks.jpeg" />
			<Image src="./assets/Betty/Yeeted into the Abyss.jpeg" />
		</Carousel>
	</div>
</section>

<style>
	#carousel {
		max-width: 33vw;
		box-shadow: -16px 10px 10px goldenrod;;
	}
	@media (max-width: 768px) {
		#carousel {
			max-width: 100vw;
		}
	}
</style>
