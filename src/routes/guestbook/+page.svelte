<script lang="ts">
	import posthog from 'posthog-js';
	import { onMount } from 'svelte';

	onMount(() => {
		posthog.capture('guestbook_viewed');
	});
</script>

<title>alexander's site</title>

<div class="guestbook">
	<iframe title="the guestbook" src="https://misscx.atabook.org/"></iframe>
</div>

<style>
	.guestbook {
		display: flex;
		justify-content: center;
	}
	iframe {
		width: 100%;
		height: 800px;
	}
</style>
