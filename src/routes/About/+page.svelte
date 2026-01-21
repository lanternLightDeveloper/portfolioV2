<script>
	import ItsMe from '$lib/img/myFace.jpg';
	import Nature1 from '$lib/img/nature1.jpg';
</script>

<svelte:head>
	<title>Lantern Light Development About</title>
	<meta
		name="description"
		content="Welcome to the Lantern Light Development about me page. This is a little bit about me."
	/>
	<meta name="keywords" content="web development, web design, software development" />
	<meta property="og:title" content="Lantern Light Development About Me" />
	<meta
		property="og:description"
		content="Welcome to the Lantern Light Development About Me page. This is a little bit about me."
	/>
	<!-- <meta property="og:image" content="$lib/img/backHero29.png" /> -->
	<meta property="og:url" content="https://www.lanternlightdevelopment.com/" />
	<meta name="twitter:card" content="$lib/img/backHero29.png" />
</svelte:head>

<header class="head_Line">
	<h1>About:</h1>
</header>

<main>
	<h1>Joel R</h1>

	<img class="face" src={ItsMe} alt="its my face" />

	<p>
		I picked up website development a few years ago. While working in a retail store. I spent down
		time learning about building a new website for the shop. Something magic happened and I easily
		found myself addicted. One realm of learning bled into another. As the wealth of knowledge grew,
		so did the interest in learning more. I've done it for fun, but I want to use my skills to help
		people who need it.
	</p>

	<p>
		I do spend some time with fun things like going to concerts, playing video games or working in
		the yard. Hiking, walking the dog and backpacking is another nice escape from everything else.
	</p>

	<img src={Nature1} alt="a sunny day on top of a mountain at a lake. It is serene" />

	<p>And a more resume version of myself</p>

	<section id="about">
		<p>
			Resilient developer with 5+ years of experience in front-end design and full stack
			development. Known for strong teamwork, communication, and problem-solving. Passionate about
			building collaborative environments and refining tools that minimize time to market.
		</p>
	</section>

	<section id="contact">
		<h2>Contact</h2>
		<ul>
			<li>Email: <a href="mailto:Joelkrivers@yahoo.com">Joelkrivers@yahoo.com</a></li>
			<li>
				Website: <a href="https://lanternlightdevelopment.com" target="_blank"
					>Lanternlightdevelopment.com</a
				>
			</li>
			<li>
				GitHub: <a href="https://github.com/Lanternlightdeveloper" target="_blank"
					>Lanternlightdeveloper</a
				>
			</li>
		</ul>
	</section>

	<section id="work-history">
		<h2>Work History</h2>
		<article>
			<h3>DebtNet (Dec 2021 - Jun 2025)</h3>
			<ul>
				<li>SQL database management for clients</li>
				<li>Front-end design and SaaS model development for Windows</li>
				<li>Software issue resolution and client support</li>
				<li>API integration and troubleshooting</li>
			</ul>
		</article>
		<article>
			<h3>Sales (Oct 2018 - 2021)</h3>
			<ul>
				<li>Customer needs assessment and solution delivery</li>
				<li>Business-to-business and retail sales experience</li>
				<li>Built trust through effective communication</li>
			</ul>
		</article>
		<article>
			<h3>Culinary (2014 - 2021)</h3>
			<ul>
				<li>Created sucess from scratch in a fast-paced kitchen</li>
				<li>Gained experience in diverse cooking styles</li>
				<li>Learned to work under pressure in team based enviroments</li>
			</ul>
		</article>
	</section>

	<section id="skills">
		<h2>Languages & Tools</h2>
		<ul>
			<li>Svelte</li>
			<li>HTML/CSS</li>
			<li>JavaScript</li>
			<li>SQL</li>
			<li>React</li>
			<li>Three.js</li>
			<li>Git</li>
			<li>Node.js</li>
			<li>Figma</li>
		</ul>
	</section>

	<section id="traits">
		<h2>Traits</h2>
		<ul>
			<li>Kindness</li>
			<li>Dependability</li>
			<li>Communication</li>
			<li>Problem-solving</li>
			<li>Resourcefulness</li>
		</ul>
	</section>

	<section id="projects">
		<h2>Projects</h2>
		<ul>
			<li>
				<strong>Lanternlightdevelopment.com</strong> - Portfolio site built with Svelte
			</li>
			<li>
				<strong><a href="https://threedlight.netlify.app"> Threedlight.netlify.app </a></strong> - 3d
				website built with Threlte using Blender assets
			</li>
			<li>
				<strong><a href="https://table-tango.netlify.app/"> Table Tango </a></strong> - Random recipe
				generator
			</li>
		</ul>
	</section>

	<section id="goals">
		<h2>Goals</h2>
		<ul>
			<li>Continue refining development skills</li>
			<li>Minimize time to market for new tools</li>
			<li>Build collaborative, creative environments</li>
			<li>Explore productive solutions through teamwork</li>
		</ul>
	</section>
</main>

<!--svelte-ignore css_unused_selector -->
<style>
	img {
		width: 60%;
		margin: 0 20%;
	}

	ul {
		margin-left: 10%;
	}

	/* Tablet Size */
	@media (min-width: 768px) {
		h1 {
			margin-bottom: -10vh;
		}
		.face {
			width: 35%;
			margin: 0 30%;
		}
	}
</style>
