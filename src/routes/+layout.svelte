<script lang="ts">
	import '../app.css';
	const { children } = $props();
</script>

<a class="logo" href="/">
	<span class="first-name">Philip</span><span class="last-name">Andersson</span>
</a>

<a class="logo-bottom" href="/">
	<span class="title-frontend">Frontend</span> <span class="title-developer">Developer</span>
</a>

<!-- <header>
	<nav>
		<a href="/portfolio" data-sveltekit-preload-data="hover">Web Developer</a>
		<a href="/writings" data-sveltekit-preload-data="hover">Writings</a>
	</nav>
</header> -->

<main>
	{@render children()}
</main>

<style>
	/*header {
		display: flex;
		justify-content: flex-end;
		align-items: center;
	}

	nav {
	}
	a {
		color: #333;
		text-decoration: none;
	}*/

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
		color: var(--accent-color);
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
	.logo-bottom {
		display: flex;
		position: fixed;
		bottom: 1rem;
		align-items: flex-end;
		right: 1rem;
		font-size: 1rem;
		color: #333;
		text-decoration: none;
		text-transform: uppercase;
		font-weight: bold;
	}
	.title-frontend {
		color: #fff;
		font-weight: bold;
		font-size: 1.5rem;
		letter-spacing: 0.25em;
		text-decoration: none;
		align-items: flex-end;
	}
	.title-developer {
		color: var(--accent-color);
		font-size: 1.5rem;
		text-orientation: upright;
		writing-mode: vertical-lr;
	}

	@media (min-width: 480px) {
		.title-frontend {
			color: #333;
		}
	}
</style>
