<script>
	import { link } from 'svelte-routing';
	const projects = [
		{
			name: "The Sketchbook Project",
			description: "artwork that calls the Brooklyn Art Library home. my physical sketchbook is currently on tour!",
			link: "https://www.sketchbookproject.com/library/21991a",
		},
		{
			name: "chananigans" ,
			description: "an idea that happened with a friend because NYC transit is oftentimes annoying.",
			link: "http://circlecircle.studio/chananigans",
		},
		{
			name: "starberry",
			description: "cHecK oUT mY sOunDCL0ud!! hahA it's ok I guess but it could be better,,,",
			link: "http://circlecircle.studio/starberry",
		},
		{
			name: "Betty",
			description: "these are completed pages of a repurposed quad notebook that I halved over time. named after a dear friend who is no longer with us.",
		},
	];
</script>

<div id="main-container">
	<section id="description-section">
		<header>
			<h1>deleting the in-between / WHAT ARE YOU DOING HERE</h1>
		</header>
		<p>setting up my own website is very time consuming and I'm pretty much exhausted all the time.</p>

		<p>I have better things to do like overshare on
			<a href="https://www.facebook.com/facebo/">Facebook</a>
		</p>

		<p>knowing me, this thing will forever be under construction - so i forced this
		<a href="https://syncretik.co">shit-eating goblin</a>
		to make it for me</p>


		<p>for now, check out some stuff I did, or tried to do:</p>
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

	</section>
	<section id="black-block">
		<footer>
			Built by Syncretik 2021, All Rights Reserved.
		</footer>
	</section>
</div>

<style>
	#main-container {
		height: 100vh;
		display: grid;
		grid-template-columns: repeat(8, minmax(10px, 1fr));
		grid-template-rows: repeat(8, minmax(10px, 1fr));
	}

	#description-section {
		margin: 0 2rem;
		grid-column: 1 / span 5;
		grid-row: 1 / span 8;
	}

	h1 {
		color: blue;
		font-size: 4em;
		font-weight: 100;
	}

	li {
			margin: 10px;
	}

 a {
		padding:3px 5px;
		color: white;
		background-color: deepskyblue;
	}
	a:hover {
		color: black;
		background-color: white;
	}

	#black-block {
		grid-column: 6 / span 3;
		grid-row: 1 / span 8;
		display: flex;
		align-items: flex-end;
		background-color: black;
		z-index: -1;
	}

  footer {
		flex: 1 0 10%;
		padding: 1rem;
		font-weight: 900;
		display: flex;
		justify-content: flex-end;
	}

</style>
