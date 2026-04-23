<script>
	import ConToTheCrete from '$lib/img/contothecrete.png';
	import TreeDfolio from '$lib/img/treedfoli.png';
	import RandReci from '$lib/img/food.png';
	import { enhance } from '$app/forms';
	import { onDestroy } from 'svelte';

	// Rolling group of words
	let entryRoller = [
		'Create',
		'Innovate',
		'Connect',
		'Share',
		'Explore',
		'Learn',
		'Grow',
		'Inspire',
		'Lead',
		'Design',
		'Build',
		'Play',
		'Dream',
		'Achieve',
		'Express',
		'Live'
	];

	let currentIndex = 0;
	let currentPhrase = $state(entryRoller[currentIndex]);

	const interval = setInterval(() => {
		currentIndex = (currentIndex + 1) % entryRoller.length;
		currentPhrase = entryRoller[currentIndex];
	}, 2000);

	onDestroy(() => {
		clearInterval(interval);
	});

	let formSubmitted = $state(false);

	const handleSubmit = () => {
		formSubmitted = true;
	};

	let isMenuOpen = $state(false);

	function toggleMenu() {
		isMenuOpen = !isMenuOpen;
	}
</script>

<svelte:head>
	<title>Lantern Light Development Homepage</title>
	<meta
		name="description"
		content="Welcome to the Lantern Light Development  homepage. Seeking to help people the way they want."
	/>
	<meta name="keywords" content="web development, web design, software development" />
	<meta property="og:title" content="Lantern Light Development Homepage" />
	<meta
		property="og:description"
		content="Welcome to the Lantern Light Development  homepage. Seeking to help people the way they want."
	/>
	<meta property="og:image" content="$lib/img/backHero443.png" />
	<meta property="og:url" content="https://www.lanternlightdevelopment.com/" />
	<meta name="twitter:card" content="$lib/img/backHero29.png" />
</svelte:head>

<header id="hero-banner" class="hero-banner">
	<h1 class="banner-text">Lantern Light Development</h1>

	<section class="banner-phrase glass-Box">
		<p class="phrase">
			<span>{currentPhrase} </span>
		</p>
		<p>the way YOU want</p>
	</section>

	<section class="banner-form">
		{#if !formSubmitted}
			<form
				class="classicForm"
				method="post"
				action="?/submit"
				use:enhance={({ formElement, formData, action, cancel }) => {
					return async ({ result, update }) => {
						if (result.type === 'success') {
							handleSubmit();
							await update();
						}
					};
				}}
				enctype="multipart/form-data"
			>
				<p>Reach out</p>
				<label for="full_name">Name</label>
				<input type="text" id="full_name" name="full_name" placeholder="Enter your name" required />

				<label for="contact_point">Email</label>
				<input
					type="text"
					id="contact_point"
					name="contact_point"
					placeholder="Enter your email"
					required
				/>

				<label for="message">Message</label>
				<textarea id="message" name="message" placeholder="Enter your message" required></textarea>

				<button class="btn-Shadow" type="submit">Submit</button>
			</form>
		{:else}
			<p class="glass-Box">Thank you for the message! I will get back to you as soon as I can.</p>
		{/if}
	</section>
</header>

<main id="main-content" class="grid-Main">
	<section class="grid-Block-Double">
		<h2>Your Partner in Making a Difference</h2>
		<p>
			Thank you for visiting. There are so many options when it comes to web development, and it can
			feel overwhelming. I'm here to make it easier. I believe in offering fair, accessible pricing,
			and I'm committed to support to those who need it. My goal is simple: to give you the tools
			you need to succeed, no matter your starting point.
		</p>
		<a href="/Contact" class="contact button-Ghost">Reach out</a>
		<ul>
			Hours of Operation:
			<li>Monday-Friday: 7:30am-6pm (Pst)</li>
			<li>Saturday & Sunday: Closed</li>
		</ul>
	</section>

	<section class="box-Contrast grid-Block-Double">
		<h2>Why would I do this?</h2>
		<p>
			I believe in helping people who are working to create a better world. Nonprofits and small
			companies often operate on tight constraints to achieve big dreams. I’m here to be an asset in
			reaching the goals you deserve.
		</p>
	</section>

	<section class="grid-Block-Double">
		<h2>Services:</h2>
		<p>
			Every project is unique, and pricing varies based on scope and complexity. My goal is to
			deliver exceptional results while keeping costs fair and equitable. All projects come with a
			free year of support to ensure your website stays up and running.
		</p>
		<button
			class="btn-Ghost"
			style="margin: 1rem 12%;"
			onclick={toggleMenu}
			onkeydown={() => (isMenuOpen = false)}
		>
			{isMenuOpen ? 'Less' : 'More'}
		</button>
		<div class:open={isMenuOpen}>
			{#if isMenuOpen}
				<section>
					<h2>Pricing Tiers</h2>

					<h3>Simple $500 - $1000</h3>
					<p>
						Perfect for those who know exactly what they need. You provide the vision, including the
						color scheme, features, and design preferences, and I bring it to life with a static or
						lightly functional website.
					</p>

					<h3>Moderate $1000 - $3000</h3>
					<p>
						Ideal if you have a general idea but need some guidance to shape your vision. Together,
						we’ll refine your ideas into a cohesive, functional website. This is going to be more
						than just a static page.
					</p>

					<h3>"I’ll Handle It" $4000+</h3>
					<p>
						For when you have a jumble of brilliant ideas but need someone to make them happen.
						We’ll collaborate to turn your concepts into a polished, professional site. This can be
						complex and include E-commerce or CMS services.
					</p>
				</section>

				<section>
					<h2>Service plan</h2>
					<p>
						Your first year of support is free. Any hiccups, issues, small changes or updates are
						covered.
						<br />
						<br />
						After the first year you can subscribe to either 6 month plan or 1 year.
					</p>
					<p>6 months is $275 1 year is $500</p>
				</section>

				<section>
					<h2>How It Works</h2>
					<p>
						I follow a structured process to ensure your project is completed efficiently and to the
						highest standard. Here's what to expect:
					</p>
					<p>
						<strong>Planning:</strong> We’ll discuss your goals, brainstorm ideas, and create a clear
						plan for your website.
					</p>
					<p>
						<strong>Design:</strong> I’ll craft a layout, color palette, and design that reflect your
						brand and message.
					</p>
					<p>
						<strong>Development:</strong> Your website will be built from the ground up, tailored to your
						specifications.
					</p>
					<p>
						<strong>Testing:</strong> Every detail will be tested across different devices and browsers
						to ensure it works seamlessly.
					</p>
					<p>
						<strong>Deployment:</strong> Your website goes live and is ready to make an impact!
					</p>
					<p>
						<strong>Support:</strong> Enjoy free support for the first year to address any unforeseen
						issues or updates.
					</p>
					<p>
						<strong>Management:</strong> Take it further with advanced features like analytics, tracking,
						and audience engagement tools.
					</p>
				</section>
			{/if}
		</div>
	</section>

	<h2 class="grid-Block-Double">Check out some of my projects:</h2>
	<section class=" projects">
		<h4>Con to the Crete.com</h4>
		<img src={ConToTheCrete} alt="Con-crete the rapper's project screenshot" />
		<p>
			A friend is a rapper who has created music for years. I made this for him to deal with merch
			sales and tour dates.
		</p>
		<a class="btn-Pulse" href="https://contothecrete.com/">Check it out</a>
	</section>

	<section class="right-Align projects">
		<h4>3D Portfolio Website</h4>
		<img src={TreeDfolio} alt="3D Portfolio Website project screenshot" />
		<p>
			I spent some time building this websites replacement in 3d. It is fully functioning. There are
			just a few things to work out.
		</p>
		<a class="btn-Pulse" href="https://threedlight.netlify.app/">Check it out</a>
	</section>

	<section class=" projects">
		<h4>Table Tango</h4>
		<img src={RandReci} alt="Table Tango project screenshot" />
		<p>
			I got tired of trying to figure out dinner. So I made a random meal generator. The initial
			version had a file full of recipes. V2 now has a login system that I made so people can
			favorite or dislike recipes. There is also user levels so people can gain the ability to
			submit recipes.
		</p>
		<a class="btn-Pulse" href="https://tester.lanternlightdevelopment.com/">Check it out</a>
	</section>
</main>

<style>
	header {
		position: relative;
		height: 100vh;
		display: grid;
		grid-template-columns: 1fr;
		grid-template-rows: 1fr 1fr 1fr;
		background-image: url('$lib/img/backHero2.png');
		background-repeat: no-repeat;
		background-attachment: fixed;
		background-position: center;
		background-size: cover;
		z-index: 999;
		color: var(--txt-2);
	}

	.banner-text {
		display: grid;
		font-size: var(--size-9);
		font-weight: 700;
	}

	.banner-phrase {
		display: grid;
		border-radius: var(--radius-S);
		align-self: center;
		justify-self: center;
		box-shadow: var(--box-Shadow);

		& p {
			font-size: var(--size-7);
			padding: var(--space-S);
			margin: 0;
		}
	}

	.phrase {
		text-decoration: underline;
		animation: slideUp 2s infinite;
	}

	@keyframes slideUp {
		0% {
			transform: translateY(100%);
			opacity: 0;
		}
		10% {
			transform: translateY(0);
			opacity: 1;
		}
		90% {
			transform: translateY(0);
			opacity: 1;
		}
		100% {
			transform: translateY(-100%);
			opacity: 0;
		}
	}

	.banner-form {
		& p {
			margin: var(--space-S);
		}
	}

	.contact {
		margin: var(--space-M);

		@media screen and (min-width: 768px) {
			margin: var(--space-Side);
		}
	}

	.projects {
		border-top: var(--border);
		border-bottom: var(--border);
		min-height: 25vh;
		margin-bottom: 5vh;

		p,
		h4 {
			padding: var(--size-4);
			font-weight: 500;
			background-color: var(--hallow);
			backdrop-filter: blur(4px);
			--webkit-backdrop-filter: blur(1.5px);
		}

		h4 {
			border-bottom: var(--border);
			width: fit-content;
		}

		a {
			margin: var(--size-4);
		}

		img {
			margin-bottom: -10vh;
		}

		@media only screen and (min-width: 768px) {
			img {
				width: 70vw;
				margin-bottom: -30vh;
			}
		}

		@media only screen and (min-width: 1024px) {
			img {
				width: 50vw;
				max-height: 350px;
			}
		}
	}

	/* Tablet  SIze  */
	@media only screen and (min-width: 766px) {
		header {
			grid-template-columns: 1fr 1fr;
			grid-template-rows: 1fr 1fr 1fr;
		}

		.banner-text {
			grid-column: span 2;
			margin: var(--space-S);
		}

		.banner-phrase {
			width: 80%;
			margin-top: -5vh;
		}

		.banner-form {
			width: 100%;
			& input,
			textarea {
				width: 100%;
			}
		}
	}

	@media only screen and (min-width: 1024px) {
		.button-Ghost {
			margin: var(--space-L);
			margin-top: -15vh;
			margin-bottom: -15vh;
		}

		.banner-phrase {
			p {
				font-size: var(--size-7);
			}
		}
	}

	/* Big screens */
	@media only screen and (min-width: 1440px) {
		.banner-text {
			padding: 0;
			margin: var(--space-Side);
			grid-row: span 2;
		}
	}
</style>
