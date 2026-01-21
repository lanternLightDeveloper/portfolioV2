<div class=" head_Line">
	<h1>County Fair</h1>
</div>

<main>
	<header>
		<h1>The New County Fair: It hurts my eyes!</h1>
		<p>
			When I went to check my local county fair website to see what times activities were scheduled.
			The website I landed on was in desperite need of an update.
		</p>
	</header>

	<section>
		<p>
			I could tell someone made it by hand and put some time into their attempt. I have spent hours
			around design and color concepts that the stucture of the page was a bit tough to see. I want
			my local spaces to be clean and wonderful. They should be something people are excited about.I
			was stuck on it in my head and so I built something a little more clean and up to date.
		</p>
	</section>

	<section>
		<h2>Date based display</h2>
		<p>The website seemed to be used for two times depending on how close it was to the fair.</p>
		<ul>
			<li>
				Most of the year it showed the last years pictures, a thank you for the year and some
				demolition derby dates.
			</li>
			<li>During the fair it was a bigger site with schedules and plans for the day and events.</li>
		</ul>
		<p>So the plan became building two zones depending on time of the year.</p>
	</section>

	<section>
		<h2>It needed</h2>
		<ul>
			<li>Color cordination</li>
			<li>Clean menu</li>
			<li>Date based pages and menu</li>
			<li>Calendar for events</li>
			<li>Pages with their own menus</li>
			<li>Data shared on multiple pages from a single source</li>
		</ul>
		<p>
			So I got to work and had fun along the way. I messed around working my way through my list and
			really hit a breaking point with Llm's. They are great, but it felt like I spent way too much
			time fixing things it changed that I did not want.
		</p>
	</section>

	<footer>
		<h2>Conclusion</h2>
		<p>
			This was a fun test of trying to build something from scratch as fast as I could. I crushed
			the time frame I would have struggled to meet in the past. I dug in to the newest styles and
			structures to grow a bit. And even if it never really gets used at least I fixed it.
		</p>
	</footer>
</main>

<!--svelte-ignore css_unused_selector -->
<style>
	header {
		& h1 {
			transform: rotate(-10deg);
		}

		margin: var(--space-Qtr);
		font-weight: bold;
	}

	ul,
	ol {
		margin: 5vh 10vw;

		@media screen and (min-width: 1024px) {
			margin: 5vh 30vw;
		}
	}

	li {
		margin: var(--size-3) 0;
	}

	img {
		width: 50vw;
		margin: var(--space-Side);
		border: var(--bord);

		@media screen and (min-width: 1440px) {
			width: 30vw;
			margin: 0 35vw;
		}
	}
</style>
