<script lang="ts">
	import './layout.css';
	import Icon from '@iconify/svelte';
	import favicon from '/favicon.ico';
	import posthog from 'posthog-js';

	let { children } = $props();

	function trackNavClick(label: string) {
		posthog.capture('nav_link_clicked', { label });
	}

	function trackSocialClick(platform: string) {
		posthog.capture('social_link_clicked', { platform });
	}
</script>

<svelte:head><link rel="icon" href={favicon} /></svelte:head>

<div class="layout-container">
	<header>
		<nav>
			<a href="/" onclick={() => trackNavClick('home')}>Home</a>
			<a href="/guestbook" onclick={() => trackNavClick('guestbook')}>Guestbook</a>
		</nav>

		<div class="social">
			<a
				href="https://hackclub.enterprise.slack.com/team/U09PHG7RLGG"
				onclick={() => trackSocialClick('slack')}
			>
				<Icon icon="mdi:slack" width="24" height="48" />
			</a>
			<a href="https://signal.me/#eu/p23SUS2Dm-maT2yMVgsr70P1vIYS2akHF3EtJrBU9s9Zl-MaKOZOoKFLEAPTbjSc" onclick={() => trackSocialClick('signal')}>
				<Icon icon="simple-icons:signal" width="24" height="48" />
			</a>
			<a href="https://t.me/coolcatsforever" onclick={() => trackSocialClick('telegram')}>
				<Icon icon="mingcute:telegram-fill" width="24" height="48" />
			</a>
			<a href="https://github.com/Snowflake6413" onclick={() => trackSocialClick('github')}>
				<Icon icon="mdi:github" width="24" height="48" />
			</a>
			<a href="mailto:riseupgang.decay960@passinbox.com" onclick={() => trackSocialClick('email')}>
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
