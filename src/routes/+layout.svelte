<script lang="ts">
	import { page } from '$app/state';
	const { children } = $props();
</script>

{#if page.url.pathname !== '/'}
<header>
	<h1>
		<a class="logo" href="/">Philip Andersson</a>
	</h1>
	<nav>
		<a href="/portfolio" data-sveltekit-preload-data="hover">Web Developer</a>
		<a href="/writings" data-sveltekit-preload-data="hover">Writings</a>
	</nav>
</header>
{/if}

<main>
	{@render children()}
</main>

<style>
	header {
		display: flex;
		justify-content: space-between;
		align-items: center;
		padding: 1rem;
		background-color: #f8f8f8;
		border-bottom: 1px solid #ddd;
	}
	nav {
		display: flex;
		gap: 1rem;
	}
	a {
		color: #333;
		text-decoration: none;
	}
	a:hover {
		color: #007bff;
	}
	.logo {
		font-size: 1.5rem;
		font-weight: bold;
		text-decoration: none;
		color: #333;
	}
	.logo:hover {
		color: #007bff;
	}
</style>
