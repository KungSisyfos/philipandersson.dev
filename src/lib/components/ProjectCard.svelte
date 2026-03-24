<script>
	const { image, title, description, siteLink = null, repoLink = null, stack } = $props();
</script>

<div class="project-card">
	<div class="project-image">
		<img src={image} alt={title} />
	</div>
	<div class="project-info">
		<h3>{title}</h3>
		<p>{description}</p>

		<ul>
			{#each stack as item, index (item)}
				{#if index > 0}&middot;{/if}
				<li>{item}</li>
			{/each}
		</ul>
		<div class="links">
			{#if siteLink}
				<a href={siteLink} target="_blank">View Site</a>
			{/if}
			{#if repoLink}
				<a href={repoLink} target="_blank">View Repository</a>
			{/if}
		</div>
	</div>
</div>

<style>
	.project-card {
		display: flex;
		flex-direction: column;
		padding: 1rem;
		margin: 2rem auto 5rem;
		min-height: 80vh;
	}
	.project-info {
		display: flex;
		flex-direction: column;
		gap: 0.5rem;
		margin-top: 0.5em;
	}
	.project-info > h3 {
		font-size: 32px;
		font-weight: 900;
		text-align: center;
	}
	.project-info > p {
		border-top: 1px solid var(--accent-color);
		border-bottom: 1px solid var(--accent-color);
		padding: 0.5rem;
		text-align: center;
	}

	.project-info > ul {
		list-style: none;
		padding: 0;
		margin: 0;
		display: flex;
		flex-wrap: wrap;
		gap: 0.5rem;
		align-items: center;
		justify-content: center;
		color: #333;
		font-weight: 500;
	}
	.project-image {
		display: flex;
		align-items: center;
		justify-content: center;
		width: 100%;
		margin: 0 auto;
	}
	.links {
		display: flex;
		gap: 1rem;
		justify-content: center;
		margin-top: 1rem;
	}
	img {
		width: 80%;
		object-fit: cover;
		filter: grayscale(100%);
	}

	img:hover {
		filter: grayscale(0%);
	}

	@media (min-width: 480px) {
		.project-card {
			align-items: center;
			justify-content: center;
			flex-direction: row;
			width: 80vw;
			margin: 0 auto;
			height: 100vh;
		}

		.project-image {
			justify-content: flex-end;
			width: 30vw;
		}

		img {
			object-fit: cover;
		}

		.project-info {
			width: 50%;
		}
	}
</style>
