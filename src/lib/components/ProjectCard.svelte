<script>
	const { image, title, description, link } = $props();
</script>

<div class="project-card">
	<div class="project-image">
		<img src={image} alt={title} />
	</div>
	<div class="project-info">
		<h3>{title}</h3>
		<p>{description}</p>
		<a href={link} target="_blank">View Project</a>
	</div>
</div>

<style>
	.project-card {
		display: flex;
		flex-direction: column;
		padding: 1rem;
		margin: 2rem auto 5rem;
		height: 100vh;
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
	.project-image {
		display: flex;
		align-items: center;
		justify-content: center;
		width: 100%;
		margin: 0 auto;
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
			margin-left: 0;
			margin-right: auto;
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
