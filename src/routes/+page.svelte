<script>
	import ProjectCard from '$lib/components/ProjectCard.svelte';

	const hourOfTheDay = new Date().getHours();
</script>

<section id="hero">
	<div class="background-image">
		<h1 class="name">
			<span class="first-name">Philip</span> <span class="last-name">Andersson</span>
		</h1>
		<h2 class="title">
			<span class="title-frontend">Frontend</span> <span class="title-developer">Developer</span>
		</h2>
	</div>
</section>

<section id="projects">
	<h2 class="projects-title"><span>Projects</span> / work</h2>
	<ProjectCard
		image="/book-binder-logo.png"
		title="Book Binder."
		description="A social book cataloging web application designed to help readers organize their personal libraries, discover new books, and connect with fellow book lovers. This is my after hours hobby project. The inspiration for this project is community-driven book sharing."
		link="https://github.com/KungSisyfos/bookbinder"
	/>
	<ProjectCard
		image="/coolstuff.png"
		title="Coolstuff"
		description="My second internship for Mediainstitutet at the company Coolstuff"
		link="https://www.coolstuff.se"
	/>
	<ProjectCard
		image="/matsedelnLogo.png"
		title="Matsedeln"
		description="For my final project at Mediainstitutet I drew on my experienes as a former cook at a preschool, and the annoyance of creating a meal plan that was varied enough and interesting enough to make the kids happy, as well as not making me and my colleague crawl up the walls. So I created Matsedeln, a meal planning web page that creates a meal plan without repetition."
		link="https://matsedeln.vercel.app/"
	/>
</section>

<section id="about">
	<div class="about-content">
		<h2>{hourOfTheDay < 12 ? 'Good morning' : 'Good afternoon'}</h2>
		<p>
			I got into frontend for practical reasons, but I found that it fits well with my love for
			stories, literature, and above all philosophy, how meaning develops through function and form.
			As a web developer that works iteratively, I like my code read and critiqued, and I build
			things I actually believe in.
		</p>
	</div>
</section>

<style>
	#hero {
		display: flex;
		flex-direction: column;
		min-height: 100vh;
	}
	#projects {
		width: 80vw;
		margin: 0 auto;
	}
	.projects-title {
		margin: 0 auto;
		text-align: center;
		text-transform: uppercase;
		text-decoration: underline;
		letter-spacing: 0.25rem;
	}
	.background-image {
		display: flex;
		flex-direction: column;
		justify-content: space-between;
		background-image: url('/hero-wide.JPG');
		background-size: cover;
		background-position: center;
		width: 100vw;
		height: 100vh;
		margin: 0 auto;
	}
	.name {
		display: none;
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
		display: none;
		padding: 0 0 0 0.5em;
		margin-bottom: 3rem;
		font-size: 1.5rem;
		text-align: center;
		color: white;
		align-items: flex-end;
		letter-spacing: 0.5em;
	}

	.title-frontend {
		color: var(--accent-color);
	}

	#about {
		background-color: #000;
		display: flex;
		flex-direction: column;
		align-items: center;
		height: 100vh;
		width: 100vw;
	}
	.about-content {
		width: 80vw;
		color: #fff;
		text-align: center;
	}

	@media (min-width: 480px) {
		:global(.project-card:nth-of-type(even)) {
			margin-left: auto;
			margin-right: 0;
			flex-direction: row-reverse;
		}
		:global(.project-card:nth-of-type(even) .project-image) {
			justify-content: flex-start;
		}

		:global(.project-card:nth-of-type(even) a) {
			text-align: right;
		}
		.background-image {
			margin: 3.5em auto;
			height: 85vh;
			width: 92vw;
		}
		.name {
			display: block;
			font-size: 5vw;
		}
		.title {
			display: block;
			font-size: 1.5rem;
			margin: 0 auto 3em;
		}
		#hero {
			margin: 0 auto;
		}
		#projects {
			width: 100vw;
		}
		.projects-title {
			font-size: 3.5rem;
		}
	}
</style>
