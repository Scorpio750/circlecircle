<script>
 import SoundcloudSVG from './SoundcloudSVG.svelte';
 import FacebookSVG from './FacebookSVG.svelte';
 import InstagramSVG from './InstagramSVG.svelte';
</script>

<section>
	<h1>Social Links</h1>
	<div id="social-links">
		<a class="social-link" href="https://www.instagram.com/copy____cat___/">
			<InstagramSVG />
		</a>
		<a  class="social-link" href="https://www.facebook.com/facebo/">
			<FacebookSVG />
		</a>
		<a  class="social-link" href="https://soundcloud.com/capybo">
			<SoundcloudSVG />
		</a>
	</div>
</section>

<style>
	section {
	}

	#social-links {
		display: flex;
		justify-content: space-around;
	}
</style>
