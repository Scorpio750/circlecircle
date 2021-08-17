<script>
	import { Link } from 'svelte-routing';
	const handleClick = e => {
		e.preventDefault();
		const img = document.getElementsByTagName('img')[0];
		console.log(img.style.opacity);
		img.style.opacity = 1;
	};
</script>

<div id="black-cover"></div>
<main>
	<h2>hey, kid.<h2>
<h2>You want some <span on:click={handleClick} id="meme-btn">memes?</span></h2>
	<img src="https://nyc3.digitaloceanspaces.com/circlecircle.studio/mtahearts.jpeg" alt="boobooboo">
<Link to="/"><button id="back-btn">Back</button></Link>
</main>

<style>
	h2 {
		font-family: "Poppins", sans-serif;
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
		width: 500px;
		opacity: 0;
		transition: all 1s;
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
		top: 2vh;
		font-size: 14px;
	}
</style>
