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
		padding: 0 5em 0 5em;
	}
	.background-image {
		background-image: url('/hero.jpg');
		background-size: cover;
		background-position: center;
		width: 80vw;
		height: 80vh;
	}
	.name {
		font-size: 8vw;
		font-weight: bolder;
		text-align: center;
	}
	.last-name {
		text-transform: uppercase;
	}

	.title {
		font-size: 2rem;
		text-align: center;
		color: white;
		align-items: flex-end;
	}
</style>
