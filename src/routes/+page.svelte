<script>
	import FairSite from '$lib/img/fairSite.png';
	import TreeDfolio from '$lib/img/treedfoli.png';
	import RandReci from '$lib/img/food.png';
	import ItsMe from '$lib/img/myFace.jpg';
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

<!--welcome info-->

<header id="hero-banner" class="hero-banner">
	<h1 class="banner-text">Lantern Light Development (TEST)</h1>

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

				<button class="ripple-btn" type="submit">Submit</button>
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
		<a href="/contact/" class="contact button-Ghost">Reach out</a>
		<ul>
			<!-- This could be a 3d neon sign with an open/closed feature -->
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
		<img src={ItsMe} alt="its my face" />

		<h2>About Me</h2>
		<p>
			I’ve spent over seven years studying and building websites, including the last few years where
			I worked at a software company learing the layers of project development. Now, I’m focused on
			putting my skills to work for people who want to make a difference in their curent life.
		</p>

		<p>Click <a href="/about/">here</a> to learn more about me.</p>
	</section>

	<h2 class="grid-Block-Double">Check out some of my projects:</h2>
	<section>
		<img src={FairSite} alt="Kitsap County Fair project screenshot" />
		<h3>County Fair</h3>
		<p>
			This is a project I used for getting up to date with different styling updates and data
			techniques.
		</p>
		<a class="pulse-button" href="https://newfaircity.netlify.app/">Check it out</a>
		<a class="pulse-button" href="/Projects/NewFairCity/">Read about this project</a>
	</section>

	<section class="right-Align">
		<img src={TreeDfolio} alt="3D Portfolio Website project screenshot" />
		<h3>3D Portfolio Website</h3>
		<p>
			I spent some time building this websites replacement in 3d. It is fully functioning. There are
			just a few things to work out.
		</p>
		<a class="pulse-button" href="https://threedlight.netlify.app/">Check it out</a>
	</section>

	<section>
		<img src={RandReci} alt="Table Tango project screenshot" />
		<h3>Table Tango</h3>
		<p>
			I got tired of trying to figure out dinner. So I made a random meal generator to get better at
			learning how to display fetched data.
		</p>
		<a class="pulse-button" href="https://table-tango.netlify.app/">Check it out</a>
	</section>
</main>

<!--svelte-ignore css_unused_selector -->
<style>
	header {
		position: relative;
		height: 100vh;
		display: grid;
		grid-template-columns: 1fr;
		grid-template-rows: 1fr 1fr 1fr;
		background-image: url('$lib/img/backHero443.png');
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
		border-radius: var(--rad-Sm);
		align-self: center;
		justify-self: center;
		box-shadow: var(--box-Shadow);

		& p {
			font-size: var(--size-7);
			padding: var(--space-Sm);
			margin: 0;
		}
	}

	.phrase {
		text-decoration: underline;
		font-size: var(--size-7);
		animation: slideUp 2s infinite;
		padding: 0;
		margin: 0;
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
			margin: var(--space-Sm);
		}
	}

	.contact {
		margin: var(--space-Med);

		@media screen and (min-width: 768px) {
			margin: var(--space-Side);
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
			margin: var(--space-Sm);
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
			margin: var(--space-Lg);
			margin-top: -15vh;
			margin-bottom: -15vh;
		}
	}

	/* Big screens */
	@media only screen and (min-width: 1440px) {
		.banner-text {
			padding: 0;
			margin: var(--space-Side);
			grid-row: span 2;
		}

		.banner-phrase {
			font-size: var(--size-8);
			margin-top: -25vh;
		}
	}
</style>
