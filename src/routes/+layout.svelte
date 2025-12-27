<script lang="ts">
	import './layout.css';
	import Icon from "@iconify/svelte";
	import favicon from '$lib/assets/favicon.svg';

	let { children } = $props();
</script>

<footer>
	<nav>
		<a href="/">Home</a>
		<a href="/contact">Contact</a>
	</nav>

	<div class="social">
		<a href="https://hackclub.enterprise.slack.com/team/U09PHG7RLGG">
		<Icon icon="mdi:slack" width="38" height="38"/>
		</a>
		<a href="/session">
		<Icon icon="simple-icons:session" width="38" height="38"/>
		</a>
	</div>
</footer>

<style>
	footer{
		display: flex;
		padding: 2rem;
		border-top: 1px solid;
		margin-top: auto;
	}
	
	nav{
		display: flex;
		gap: 1rem;
		margin-bottom: 1rem;
	}

	.social{
		display:flex;
		gap: 1rem;
		margin-left: auto;
	}
</style>

<svelte:head><link rel="icon" href={favicon} /></svelte:head>
{@render children()}
