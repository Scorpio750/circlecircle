
<div class="text-tile">
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
</div>
