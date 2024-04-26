<script>
 import SoundcloudSVG from './SoundcloudSVG.svelte';
 import FacebookSVG from './FacebookSVG.svelte';
 import InstagramSVG from './InstagramSVG.svelte';
 import PaypalSVG from './PaypalSVG.svelte';
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
		<a class="social-link" href="https://paypal.me/circlecirclestudio">
			<PaypalSVG />
		</a>
	</div>
</section>

<style>
	section {}

	h1 {
		font-size: 1.7em;
	}

	#social-links {
		display: flex;
		justify-content: space-around;
		margin: 1em;
	}

	@media (max-width: 999px) {
		#social-links {
			flex-wrap: wrap;
		}
	}
</style>
