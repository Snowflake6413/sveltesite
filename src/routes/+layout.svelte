<script lang="ts">
	import './layout.css';
	import Icon from "@iconify/svelte";
	import favicon from '/favicon.ico';

	let { children } = $props();
</script>

<footer>
	<nav>
		<a href="/">Home</a>
		<a href="/guestbook">Guestbook</a>
	</nav>

	<div class=aga>
			<h1>the site of alexander :3 </h1>
	</div>

	<div class="social">
		<a href="https://hackclub.enterprise.slack.com/team/U09PHG7RLGG">
		<Icon icon="mdi:slack" width="24" height="48"/>
		</a>
		<a href="/session">
		<Icon icon="simple-icons:session" width="24" height="48"/>
		</a>
		<a href="https://github.com/Snowflake6413">
		<Icon icon="mdi:github" width="24" height="48" />
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
	.aga{
		text-align: center;
		margin: auto;
	}
</style>

<svelte:head><link rel="icon" href={favicon} /></svelte:head>
{@render children()}
