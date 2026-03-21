<script>
	import ProjectCard from '$lib/components/ProjectCard.svelte';

	import Mail from '@lucide/svelte/icons/mail';

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
		<h2>Thank you for visiting!</h2>
		<p>
			I got into frontend for practical reasons, but found that it suits me well. With my love of
			stories, literature, and philosophy, I'm looking for a team that cares about craft and
			building things that are both useful and worth using. If this interests you, please feel free
			to reach out.
		</p>
		<p>
			And I hope that you have a {hourOfTheDay < 12
				? 'good morning'
				: hourOfTheDay < 18
					? 'good afternoon'
					: 'good evening'}
		</p>
	</div>
	<div class="links">
		<a href="https://github.com/KungSisyfos" aria-label="github link">
			<svg
				xmlns="http://www.w3.org/2000/svg"
				width="24"
				height="24"
				viewBox="0 0 98 96"
				fill="currentColor"
			>
				<path
					d="M48.854 0C21.839 0 0 22 0 49.217c0 21.756 13.993 40.172 33.405 46.69 2.427.49
  3.316-1.059 3.316-2.362 0-1.141-.08-5.052-.08-9.127-13.59
  2.934-16.42-5.867-16.42-5.867-2.184-5.704-5.42-7.17-5.42-7.17-4.448-3.015.324-3.015.324-3.015
  4.934.326 7.523 5.052 7.523 5.052 4.367 7.496 11.404 5.378 14.235 4.074.404-3.178 1.699-5.378
  3.074-6.6-10.839-1.141-22.243-5.378-22.243-24.283 0-5.378 1.94-9.778
  5.014-13.2-.485-1.222-2.184-6.275.486-13.038 0 0 4.125-1.304 13.426 5.052a46.97 46.97 0 0 1
  12.214-1.63c4.125 0 8.33.571 12.213 1.63 9.302-6.356 13.427-5.052 13.427-5.052 2.67 6.763.97
  11.816.485 13.038 3.155 3.422 5.015 7.822 5.015 13.2 0 18.905-11.404 23.06-22.324 24.283 1.78
  1.548 3.316 4.481 3.316 9.126 0 6.6-.08 11.897-.08 13.526 0 1.304.89 2.853 3.316 2.364
  19.412-6.52 33.405-24.935 33.405-46.691C97.707 22 75.788 0 48.854 0z"
				/>
			</svg>
		</a>

		<a href="https://www.linkedin.com/in/philip-andersson-022549228/" aria-label="linkedin link">
			<svg
				xmlns="http://www.w3.org/2000/svg"
				width="24"
				height="24"
				viewBox="0 0 24 24"
				fill="currentColor"
				overflow="visible"
			>
				<path
					d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136
  1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267
  2.37 4.267 5.455v6.286zM5.337 7.433a2.062 2.062 0 0 1-2.063-2.065 2.064 2.064 0 1 1 2.063
  2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0
  23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222
  0h.003z"
				/>
			</svg>
		</a>
		<a href="mailto:ph.andersson@proton.me"><Mail /></a>
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
		justify-content: center;
		height: 100vh;
		width: 100vw;
		gap: 5rem;
	}
	.about-content {
		width: 80vw;
		color: #fff;
		text-align: center;
	}
	.links {
		display: flex;
		justify-content: center;
		gap: 3rem;
		color: #fff;
	}
	.links a {
		color: #fff;
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
