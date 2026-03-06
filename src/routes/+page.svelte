<script>
	import { fade } from 'svelte/transition';
	import { onMount } from 'svelte';

	let dotCount = $state(0);

	onMount(() => {
		const interval = setInterval(() => {
			dotCount = dotCount >= 3 ? 0 : dotCount + 1;
		}, 600);
		return () => clearInterval(interval);
	});

	let dots = $derived(Array.from({ length: dotCount }, (_, i) => i));
</script>

<section>
	<p class="domain">https://philipandersson.dev</p>
	<p class="status">
		coming soon{#each dots as i (i)}<span in:fade={{ duration: 400 }} out:fade={{ duration: 200 }}
				>.</span
			>{/each}
	</p>
</section>

<style>
	:global(body) {
		margin: 0;
		background: #000;
	}

	:global(main) {
		display: flex;
		justify-content: center;
		align-items: center;
		height: 100vh;
	}

	section {
		display: flex;
		flex-direction: column;
		align-items: center;
		font-family: 'Courier New', Courier, monospace;
		color: #00ff41;
	}

	.domain {
		font-size: 2.5rem;
		margin: 0 0 0.5rem 0;
		letter-spacing: 0.05em;
	}

	.status {
		font-size: 1.2rem;
		margin: 0;
		letter-spacing: 0.1em;
	}

	span {
		display: inline-block;
	}
</style>
