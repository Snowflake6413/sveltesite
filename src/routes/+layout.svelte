<script lang="ts">
	import './layout.css';
	import Icon from '@iconify/svelte';
	import favicon from '/favicon.ico';

	let { children } = $props();
</script>

<svelte:head><link rel="icon" href={favicon} /></svelte:head>

<div class="layout-container">
	<header>
		<nav>
			<a href="/">Home</a>
			<a href="/guestbook">Guestbook</a>
		</nav>


		<div class="social">
			<a href="https://hackclub.enterprise.slack.com/team/U09PHG7RLGG">
				<Icon icon="mdi:slack" width="24" height="48" />
			</a>
			<a href="/session">
				<Icon icon="simple-icons:session" width="24" height="48" />
			</a>
			<a href="https://github.com/Snowflake6413">
				<Icon icon="mdi:github" width="24" height="48" />
			</a>
			<a href="mailto:me@ifeellikeharukananase.tech">
				<Icon icon="ic:outline-email" width="24" height="48" />
			</a>
		</div>
	</header>

	<main>
		{@render children()}
	</main>
</div>

<style>
	.layout-container {
		display: flex;
		flex-direction: column;
		min-height: 100vh;
	}

	header {
		display: flex;
		padding: 2rem;
		border-bottom: 1px solid;
	}

	main {
		flex: 1;
	}

	nav {
		display: flex;
		gap: 1rem;
		margin-bottom: 1rem;
	}

	.social {
		display: flex;
		gap: 1rem;
		margin-left: auto;
	}
</style>
