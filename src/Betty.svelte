<script>
	import { onMount } from 'svelte';
	import { Link } from 'svelte-routing';
	import { PageFlip } from 'page-flip';
	import BackButton from './BackButton.svelte';

	onMount(async () => {
		const book = document.querySelector('#flipbook');
		const pageFlip = new PageFlip(book, {
			width: 360,
			height: 340,
			maxShadowOpacity: 0.5, // Half shadow intensity
		});
		pageFlip.loadFromImages([
			'./assets/Betty/A Cloudy Day by the Sea.jpeg',
			'./assets/Betty/Cactus Dance II.jpeg',
			'./assets/Betty/Cactus Dance.jpeg',
			'./assets/Betty/Cloud Garden.jpeg',
			'./assets/Betty/Colorcruise.jpeg',
			'./assets/Betty/Cosmic Dust.jpeg',
			'./assets/Betty/Darkness Creeps In.jpeg',
			'./assets/Betty/Deathstar.jpeg',
			'./assets/Betty/Discovery.jpeg',
			'./assets/Betty/Diver.jpeg',
			'./assets/Betty/Everything Dies.jpeg',
			'./assets/Betty/Falling Off the Canvas.jpeg',
			'./assets/Betty/Flora.jpeg',
			'./assets/Betty/Funnel.jpeg',
			'./assets/Betty/Jitters.jpeg',
			'./assets/Betty/Kestrel.jpeg',
			'./assets/Betty/Kineticity.jpeg',
			'./assets/Betty/King Frog.jpeg',
			'./assets/Betty/Last of the Dinosaurs.jpeg',
			'./assets/Betty/Mecharoot.jpeg',
			'./assets/Betty/Mesh Potatoes.jpeg',
			'./assets/Betty/New Perspective.jpeg',
			'./assets/Betty/Roads that Lead to Something.jpeg',
			'./assets/Betty/Serpentine.jpeg',
			'./assets/Betty/Shirley & the Medium Hypnosis.jpeg',
			'./assets/Betty/Space Junk.jpeg',
			'./assets/Betty/Tangle.jpeg',
			'./assets/Betty/This Could Be Sexual.jpeg',
			'./assets/Betty/Unstructural Sound.jpeg',
			'./assets/Betty/Valleys & Peaks.jpeg',
			'./assets/Betty/Yeeted into the Abyss.jpeg',
			'./assets/Betty/the-end.jpeg',
		]);
	});
</script>

<main id="table">
	<div id="flipbook">
	</div>
	<BackButton />
</main>

<style>
	#table {
		min-height: 100vh;
		overflow: hidden;
		width: 100vw;
		display: flex;
		justify-content: center;
		align-items: center;
		background-color: white;
	}
</style>
