<script lang="ts">
	const { children } = $props();
</script>

<a class="logo" href="/">
	<span class="first-name">Philip</span><span class="last-name">Andersson</span>
</a>

<header>
	<nav>
		<a href="/portfolio" data-sveltekit-preload-data="hover">Web Developer</a>
		<a href="/writings" data-sveltekit-preload-data="hover">Writings</a>
	</nav>
</header>

<main>
	{@render children()}
</main>

<style>
	:global(*) {
		margin: 0;
		padding: 0;
	}
	:global(body) {
		font-family: 'Inconsolata', monospace;
	}
	header {
		display: flex;
		justify-content: flex-end;
		align-items: center;
		padding: 1rem;
	}

	nav {
		display: flex;
		margin-top: 3rem;
		flex-direction: column;
		align-items: flex-end;
		gap: 1rem;
	}
	a {
		color: #333;
		text-decoration: none;
	}
	a:hover {
		text-decoration: underline;
	}
	.logo {
		position: fixed;
		top: 1rem;
		left: 1rem;
		display: flex;
		align-items: flex-start;
		font-size: 1.5rem;
		font-weight: bold;
		text-decoration: none;
		color: #333;
	}
	.logo:hover {
		color: #007bff;
		text-decoration: none;
	}
	.first-name {
		font-weight: bold;
		writing-mode: vertical-rl;
		text-orientation: upright;
		text-transform: uppercase;
	}
	.last-name {
		text-transform: uppercase;
		letter-spacing: 0.25em;
		margin-left: 0.75em;
	}
</style>
