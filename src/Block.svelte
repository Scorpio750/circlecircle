<section id="black-block">
	<footer>
		Built by <a href="https://syncretik.co">[Syncretik]</a> 2021, All Rights Reserved.
	</footer>
</section>

<style>
	section {
		/* animation: waver .0001s ease-out alternate infinite; */
		background-image:  repeating-radial-gradient( circle at 0 0, transparent 0, #e5e5f7 100px ), repeating-linear-gradient( yellow, lightyellow );
		grid-column: 6 / span 4;
		grid-row: 1 / span 8;
		display: flex;
		align-items: flex-end;
		background-color: black;
		min-height: 10%;
		z-index: -1;
	}

	section a {
		padding: 0 5px;
		text-decoration: none;
		background-color: inherit;
		color: dimgrey;
	}

	section a:hover {
		color: grey;
	}

  footer {
		flex: 1 0 10%;
		opacity: 1;
		background-color: black;
		padding: 1rem;
		font-weight: 900;
		display: flex;
		justify-content: flex-end;
	}
</style>

