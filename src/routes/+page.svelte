<script>
</script>

<section id="hero">
	<div class="background-image">
		<h1 class="name">
			<span class="first-name">Philip</span> <span class="last-name">Andersson</span>
		</h1>
		<h2 class="title">Junior Frontend Developer</h2>
	</div>
</section>

<style>
	#hero {
		display: flex;
		flex-direction: column;
		margin: 0 auto;
	}
	.background-image {
		display: flex;
		flex-direction: column;
		justify-content: space-between;
		background-image: url('/hero-wide.JPG');
		background-size: cover;
		background-position: center;
		width: 100vw;
		height: 60vh;
		margin: 0 auto;
	}
	.name {
		color: #000;
		font-size: 9vw;
		font-weight: bolder;
		text-align: center;
		margin-top: 5rem;
	}

	.first-name {
		text-transform: uppercase;
	}
	.last-name {
		text-transform: uppercase;
	}

	.title {
		padding: 0 0 0 0.5em;
		margin-bottom: 3rem;
		font-size: 1.5rem;
		text-align: center;
		color: white;
		align-items: flex-end;
		letter-spacing: 0.5em;
	}

	@media (min-width: 480px) {
		.background-image {
			margin: 3em auto;
			width: 80vw;
			height: 70vh;
		}
		.name {
			font-size: 5vw;
		}
		.title {
			font-size: 1.5rem;
			margin: 0 auto 3em;
		}
	}
</style>
