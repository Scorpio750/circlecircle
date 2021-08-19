<script>
	import projects from './projects.js';
	import { link } from 'svelte-routing';
</script>

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

		<div id="horizontal-spacer" />

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

<style>
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
		background-color: deepskyblue;
	}
	a:hover {
		color: black;
		background-color: white;
	}

	#horizontal-spacer {
		margin: 3rem 0;
		width: 8rem;
		height: 2rem;
		background-color: black;
	}
</style>
