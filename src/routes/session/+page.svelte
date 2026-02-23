<script lang="ts">
	import posthog from 'posthog-js';
	import { onMount } from 'svelte';

	onMount(() => {
		posthog.capture('session_contact_viewed');
	});
</script>

<title>alexander's site</title>

<div class="sessionqr">
	<h1>Session Contact</h1>
	<p>
		Since I cannot share a link to my Session link, here is a QR code that you can scan to chat with
		me! :3
	</p>

	<img
		src="https://hc-cdn.hel1.your-objectstorage.com/s/v3/6f8ad79a4625586f_static-qr-code-5c947467fc92a0e2f26bd654c8af44d9.svg"
		alt="Session QR Code"
		width="348"
		height="348"
	/>
	<p>miss cx</p>
</div>

<style>
	:global(body) {
		background-color: #7bc4c4;
	}
	.sessionqr {
		border: 1px solid #333;
		padding: 20px;
	}
</style>
