<script>
	function handleMove(e) {
		const rect = e.currentTarget.getBoundingClientRect();
		const x = e.clientX - rect.left;
		const y = e.clientY - rect.top;

		e.currentTarget.style.setProperty('--x', `${x}px`);
		e.currentTarget.style.setProperty('--y', `${y}px`);
		e.currentTarget.style.setProperty('--glow-opacity', 1);
	}

	function handleLeave(e) {
		e.currentTarget.style.setProperty('--glow-opacity', 0);
	}
</script>

<main class="cv">
	<section class="hero">
		<h1>Joel Rivers</h1>
		<p class="title">Frontend Developer | Svelte • JavaScript • SQL</p>
		<p class="summary">
			I have built websites for eight years as a frontend focused developer. Three and a half of
			those year's was spent working at a company that made software for debt collection agencies.
		</p>
	</section>

	<section
		class="card"
		on:mousemove={handleMove}
		on:mouseleave={handleLeave}
		aria-labelledby="work-history"
	>
		<h2 id="work-history">Work History</h2>

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

	<section class="card traits-focus">
		<ul class="traits" on:mousemove={handleMove} on:mouseleave={handleLeave}>
			<h2>Strengths</h2>
			{#each ['Dependability', 'Communication', 'Kindness', 'Perseverance', 'Moldable', 'Curious', 'Aware', 'Composed'] as trait (trait)}
				<li>{trait}</li>
			{/each}
		</ul>
	</section>

	<section
		class="card"
		on:mousemove={handleMove}
		on:mouseleave={handleLeave}
		aria-labelledby="skills-tools"
	>
		<h2 id="skills-tools">Tech Skill's & tools</h2>

		<div class="skills-graph">
			<div class="skill" style="--level: 8">
				<span>Semantic HTML/CSS</span>
				<div class="bar"></div>
			</div>

			<div class="skill" style="--level: 8">
				<span>Node.js</span>
				<div class="bar"></div>
			</div>

			<div class="skill" style="--level: 7">
				<span>JavaScript</span>
				<div class="bar"></div>
			</div>

			<div class="skill" style="--level: 7">
				<span>Accessibility</span>
				<div class="bar"></div>
			</div>

			<div class="skill" style="--level: 6">
				<span>Git</span>
				<div class="bar"></div>
			</div>

			<div class="skill" style="--level: 6">
				<span>Svelte</span>
				<div class="bar"></div>
			</div>

			<div class="skill" style="--level: 4">
				<span>Three.js</span>
				<div class="bar"></div>
			</div>

			<div class="skill" style="--level: 4">
				<span>Visual FoxPro</span>
				<div class="bar"></div>
			</div>

			<div class="skill" style="--level: 4">
				<span>MySQL</span>
				<div class="bar"></div>
			</div>

			<div class="skill" style="--level: 3">
				<span>React</span>
				<div class="bar"></div>
			</div>

			<div class="skill" style="--level: 2">
				<span>PostgreSQL</span>
				<div class="bar"></div>
			</div>

			<div class="skill" style="--level: 2">
				<span>Figma</span>
				<div class="bar"></div>
			</div>
		</div>
	</section>

	<section
		class="card"
		on:mousemove={handleMove}
		on:mouseleave={handleLeave}
		aria-labelledby="projects-heading"
	>
		<h2 id="projects-heading">Projects</h2>

		<ul class="projects">
			<li>
				<h3>
					<a class="btn btn-rise" href="https://lanternlightdevelopment.com">
						Lanternlightdevelopment.com
					</a>
				</h3>
				<p>My personal page for freelance web development.</p>
				<ul>
					<li>Coolify + Svelte + Supabase</li>
					<li>Login and message system</li>
					<li>Contact points</li>
				</ul>
			</li>

			<li>
				<h3>
					<a class="btn btn-rise" href="https://contothecrete.com"> ConToTheCrete.com </a>
				</h3>
				<p>Con-Crete the rapper's website for merch and ticket sales.</p>
				<ul>
					<li>Netlify + Svelte + Square</li>
					<li>Sales point for CD and clothing sales</li>
					<li>Concert data</li>
					<li>Fan Gallery</li>
				</ul>
			</li>

			<li>
				<h3>
					<a class="btn btn-rise" href="https://table-tango.netlify.app/"> Table Tango </a>
				</h3>
				<p>A recipe randomizer for messing with login systems and databases.</p>
				<ul>
					<li>Coolify + Svelte + PostgreSQL</li>
					<li>Login</li>
					<li>Users/Admin</li>
					<li>Recipe randomizer/cookbook</li>
					<li>Favorites/dislikes</li>
					<li>Recipe submission</li>
					<li>User roles</li>
				</ul>
			</li>
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
		position: relative;
		overflow: hidden;
		perspective: 800px;
		cursor: none;

		&::before {
			content: '';
			position: absolute;
			inset: 0;

			background: radial-gradient(
				100px circle at var(--x) var(--y),
				var(--accent-1),
				transparent 60%
			);

			opacity: var(--glow-opacity, 0);
			transition:
				opacity 0.25s ease,
				background 0.1s;

			pointer-events: none;
		}
	}

	.traits-focus {
		padding: 0;
		margin: 0;
	}

	.traits {
		display: grid;
		grid-template-columns: repeat(2, 1fr);
		gap: 0.75rem;
		padding: 1.5rem;
		margin: 0;
		perspective: 800px;
		cursor: none;

		li {
			list-style: none;
			padding: 1rem;
			border-radius: 14px;
			border: var(--border-2);
			text-align: center;
			transform-style: preserve-3d;
			transition:
				transform 0.25s ease,
				background 0.25s ease,
				color 0.25s ease,
				opacity 0.25s ease,
				box-shadow 0.25s ease;

			&&:hover {
				opacity: 1;
				filter: blur(0);

				background: linear-gradient(135deg, var(--accent-2), var(--accent-1));
				transform: translateZ(20px) rotateX(3deg) rotateY(-7deg) scale(1.08);
			}
		}

		&:hover li {
			opacity: 0.25;
			filter: blur(1px);
		}

		&::before {
			content: '';
			position: absolute;
			inset: 0;

			background: radial-gradient(
				100px circle at var(--x) var(--y),
				var(--accent-1),
				transparent 60%
			);

			opacity: var(--glow-opacity, 0);
			transition:
				opacity 0.25s ease,
				background 0.1s;

			pointer-events: none;
		}

		@media only screen and (min-width: 768px) {
			grid-template-columns: repeat(3, 1fr);
		}
	}

	.skills-graph {
		display: flex;
		flex-direction: column;
		gap: 0.8rem;
	}

	.skill {
		display: flex;
		flex-direction: column;
		gap: 0.2rem;
		font-size: 0.9rem;
	}

	.skill span {
		display: flex;
		justify-content: space-between;
	}

	.bar {
		height: 6px;
		background: var(--bg-1);
		border-radius: 4px;
		overflow: hidden;
		position: relative;
	}

	.bar::after {
		content: '';
		position: absolute;
		inset: 0;
		width: calc(var(--level) * 12.5%);
		background: linear-gradient(90deg, var(--accent-2), var(--accent-1));
		border-radius: 4px;
		transition: width 0.6s ease;
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

	.projects li {
		margin-bottom: 1rem;
	}

	.projects p {
		margin: 0.3rem 0 0;
	}

	.projects a {
		text-shadow: var(--shadow-Txt);
	}
</style>
