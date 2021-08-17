<script>
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
	];
</script>
<section>
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
		<a target="_blank" href={project.link}>
			{project.name}
		</a>
		- {project.description}
	</li>
	{/each}

</section>

<style>
	a {
		color: white;
		background-color: black;
	}
	a:hover {
		color: black;
		background-color: white;
	}

	project {
		font-family: monospace;
	}
</style>
