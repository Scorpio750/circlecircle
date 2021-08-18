<script>
	import { tweened } from 'svelte/motion';
	import { cubicOut } from 'svelte/easing';
	import { Link } from 'svelte-routing';
	import { onMount } from 'svelte';

	let wew;
	let frogeDance;

	onMount(async () => {
		wew = await createBufferedAudioSource('./assets/wew.mp3', 2.0);
		frogeDance = await createBufferedAudioSource('./assets/froge_dance.mp3', 1.5);
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

	const getRandomCoordinates = max => Math.floor(Math.random() * (max));
	const scaleToFit = (img, canvas, ctx) => {
    // get the scale
    const scale = Math.min(canvas.width / img.width, canvas.height / img.height);
    // get the top left position of the image
    const x = (canvas.width / 2) - (img.width / 2) * scale;
    const y = (canvas.height / 2) - (img.height / 2) * scale;
    ctx.drawImage(img, x, y, img.width * scale, img.height * scale);
	}

	const selfDestruct = () => {
		wew.start();
		alert('byebye ^_^');
		const spine = document.querySelector('main');
		spine.parentNode.removeChild(spine);

		const body = document.querySelector('body');
		const froge = new Image();
		froge.src = "./assets/froge.gif";
		froge.style.width = "100vw";
		froge.style.height = "100vh";
    body.append(froge);
		frogeDance.start();
	}

	const handleClick = e => {
		e.preventDefault();

		const patientZero = document.querySelector('img');
		const patientCoordinates = patientZero.getBoundingClientRect();

		let memeArmy = 0;
			setInterval(() => {
				const freshZombie = document.createElement('canvas');
				const ctx = freshZombie.getContext('2d');
				scaleToFit(patientZero, freshZombie, ctx);

				freshZombie.style.position = 'absolute';
				freshZombie.style.zIndex = getRandomCoordinates();

				const newLeft = getRandomCoordinates(window.innerWidth - 300);
				const newTop = getRandomCoordinates(window.innerHeight - 150);

				freshZombie.style.left = `${newLeft >= 0 ? newLeft : 0}px`;
				freshZombie.style.top = `${newTop >= 0 ? newTop : 0}px`;
				patientZero.parentNode.insertBefore(freshZombie, patientZero.nextSibling);
				if (memeArmy === 420) {
					clearInterval();
					selfDestruct();
				}
				memeArmy++;
			}, 5);
	};

	const progress = tweened(0, {
		duration: 400,
		easing: cubicOut
	});
</script>

<div id="black-cover"></div>
<main>
	<h2>hey, kid.<h2>
	<h2>You want some <span on:click={handleClick} id="meme-btn">memes?</span></h2>
	<Link to="/"><button id="back-btn">Back</button></Link>
</main>

<img src="https://nyc3.digitaloceanspaces.com/circlecircle.studio/mtahearts.jpeg" alt="boobooboo">

<style>
	h2 {
		font-family: 'Barrio';
	}

	#black-cover {
		position: absolute;
		top: 0;
		left: 0;
		width: 100vw;
		height: 100vh;
		background-color: black;
		z-index: -1;
	}

	main {
		display: flex;
		flex-flow: column nowrap;
		justify-content: center;
		align-items: center;
	}

	img {
		display: none;
		position: absolute;
		left: 50%;
		top: 50%;
	}

	#meme-btn {
		color: red;
		transition: all .3s;
	}

	#meme-btn:hover {
		color: fuchsia;
		font-style: oblique;
		cursor: pointer;
	}

	#back-btn {
		position: absolute;
		left: 3vh;
		bottom: 1vh;
		font-size: 18px;
		font-family: sans-serif;
	}
</style>
