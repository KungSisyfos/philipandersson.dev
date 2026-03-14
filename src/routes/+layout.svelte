<script lang="ts">
	const { children } = $props();
</script>

<header>
	<h1>
		<a class="logo" href="/">
			<span class="first-name">Philip</span><span class="last-name">Andersson</span>
		</a>
	</h1>
	<nav>
		<a href="/portfolio" data-sveltekit-preload-data="hover">Web Developer</a>
		<a href="/writings" data-sveltekit-preload-data="hover">Writings</a>
	</nav>
</header>

<main>
	{@render children()}
</main>

<style>
	:global(body) {
		font-family: 'Inconsolata', monospace;
	}
	header {
		display: flex;
		justify-content: space-between;
		align-items: center;
		padding: 1rem;
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
		position: sticky;
		display: flex;
		align-items: flext-start;
		font-size: 1.5rem;
		font-weight: bold;
		text-decoration: none;
		color: #333;
	}
	.logo:hover {
		color: #007bff;
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
