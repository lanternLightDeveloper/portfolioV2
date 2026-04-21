<main class="cv">
	<section class="hero">
		<h1>Joel Rivers</h1>
		<p class="title">Frontend Developer | Svelte • JavaScript • SQL</p>
		<p class="summary">
			I have built websites for eight years as a frontend focused developer. Three and a half of
			those year's was spent working at a company that made software for debt collection agencies.
		</p>
	</section>

	<section class="card">
		<h2>Tech Skill's & tools</h2>
		<div class="skills">
			<span>Semantic HTML/CSS (8 yrs)</span>
			<span>Node.js (8 yrs)</span>
			<span>JavaScript (7 yrs)</span>
			<span>Accessibility (7 yrs)</span>
			<span>Git (6 yrs)</span>
			<span>Svelte (6 yrs)</span>
			<span>Three.js (4 yrs)</span>
			<span>Visual FoxPro (4 yrs)</span>
			<span>MySQL (4 yrs)</span>
			<span>React (3 yrs)</span>
			<span>PostgreSQL (2 yrs)</span>
			<span>Figma (2 yrs)</span>
		</div>
	</section>

	<section class="card">
		<h2>Projects</h2>
		<ul class="projects">
			<strong>Lanternlightdevelopment.com</strong>
			<p>My personal page for freelance web development.</p>
			<li>Coolify + Svelte + Supabase</li>
			<li>Login and message system</li>
			<li>Contact points</li>
			<strong><a href="https://ConToTheCrete.com">ConToTheCrete.com</a></strong>
			<p>Con-Crete the rappers website for merch and ticket sales.</p>
			<li>Netlify + Svelte + Square</li>
			<li>Sales point for Cd and clothing sales</li>
			<li>Concert data</li>
			<li>Fan Gallery</li>

			<strong><a href="https://table-tango.netlify.app/">Table Tango</a></strong>
			<p>A recipe randomizer for messing with login systems and databases.</p>
			<li>Coolify + Svelte + PostgreSQL</li>
			<li>Login</li>
			<li>Users/ Admin</li>
			<li>Recipe randomizer/cookbook</li>
			<li>recipe favorite/dislike button</li>
			<li>Recipe submission</li>
			<li>User levels for admin/moderator/user/guest</li>
		</ul>
	</section>

	<section class="card">
		<h2>Work History</h2>

		<article>
			<h3>DebtNet <span>(2021 – 2025)</span></h3>
			<ul>
				<li>MySql structured database management</li>
				<li>Software issue resolution</li>
				<li>Crisis de-escalation</li>
			</ul>
			<p>
				Debt$Net is a software built with Visual FoxPro and MySql for Windows. As part of the
				support team I was the first person at the phone for issue's with systems and databases.
				From "Oh no, I messed up and changed all of the dates in the initial_in column" to "every
				day we log in, yesterdays work is gone". When the world was not on fire I learned coding
				through hands on problem solving such as working on a team to fix an Experian Api connection
				issue or writing scripts in Visual FoxPro to transfer data from a file into the customer's
				database.
			</p>
		</article>

		<article>
			<h3>Sales <span>(2018 – 2021)</span></h3>
			<ul>
				<li>Consumer interests</li>
				<li>Design aesthetics</li>
				<li>Human relations</li>
			</ul>
		</article>

		<article>
			<h3>Culinary <span>(2014 – 2021)</span></h3>
			<ul>
				<li>Task managment</li>
				<li>Team goal setting</li>
				<li>Time efficiency</li>
			</ul>
		</article>
	</section>

	<section class="card">
		<h2>Strengths</h2>
		<ul class="traits">
			<li>Dependability</li>
			<li>Communication</li>
			<li>Kindness</li>
			<li>Perseverance</li>
			<li>Moldable</li>
			<li>Curious</li>
			<li>Aware</li>
			<li>Composed</li>
			<li>Strategic</li>
		</ul>
	</section>
</main>

<style>
	.cv {
		max-width: 900px;
		margin: auto;
		padding: var(--size-7);
		display: grid;
		gap: var(--size-7);
	}

	.hero h1 {
		font-size: 2.5rem;
		margin-bottom: 0.5rem;
	}

	.title {
		font-weight: bold;
		color: var(--accent-1);
	}

	.summary {
		margin-top: 1rem;
		max-width: 600px;
	}

	.card {
		padding: 1.5rem;
		border-radius: var(--radius-S);
		background: var(--bg-2);
	}

	.skills {
		display: flex;
		flex-wrap: wrap;
		gap: 0.5rem;
	}

	.skills span {
		background: var(--bg-1);
		padding: 0.4rem 0.7rem;
		border: var(--border);
		border-radius: 6px;
		font-size: 0.9rem;
	}

	.projects li {
		margin-bottom: 1rem;
	}

	.projects p {
		margin: 0.3rem 0 0;
	}

	.projects a {
		text-shadow: var(--shadow-Txt);
	}

	article {
		margin-bottom: 1.5rem;
	}

	article h3 {
		display: flex;
		justify-content: space-between;
		font-size: 1.1rem;
	}

	article span {
		color: var(--txt-2);
		font-weight: normal;
	}

	.traits {
		display: flex;
		flex-wrap: wrap;
		gap: 0.5rem;
	}

	.traits li {
		background: var(--bg-1);
		padding: 0.4rem 0.7rem;
		border-radius: 6px;
		border: var(--border);
	}
</style>
