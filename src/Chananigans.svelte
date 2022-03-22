<script>
	import { onMount } from 'svelte';
	import { flip } from 'svelte/animate';
	import BackButton from './BackButton.svelte';

	let catDance;
	const vids = new Array(8).fill({ muted: true });
	vids[2] = { muted: false }

	onMount(async () => {
		/* catDance = await createBufferedAudioSource('./assets/cat-dance.mp3', 1); */
		/* catDance.start(0, 48); */
	});

	const createBufferedAudioSource = async (path, rate) => {
		const AudioContext = window.AudioContext || window.webkitAudioContext;
		const audioCtx = new AudioContext();
		const source = audioCtx.createBufferSource();

		const req = new Request(path);
		const res = await fetch(req);
		const buffer = await res.arrayBuffer();
		audioCtx.decodeAudioData(buffer, function(decodedData) {
      source.buffer = decodedData;
      source.connect(audioCtx.destination);
    });
    source.playbackRate.value = rate;
		return source;
	}
</script>

<main>
	{#each vids as vid}
		<video muted={vid.muted} autoplay loop=true src="./assets/cat-dance.mp4" />
	{/each}
	<BackButton />
</main>


<style>
	main {
		background-color: black;
	}

	video {
		display: inline-block;
	}
</style>
