<script>
	import Wsrd from '$lib/img/wsrd.png';
	import ArtCount from '$lib/img/artCountV4.png';
	import RandReci from '$lib/img/food.png';
	import RandShop from '$lib/img/shoppo.png';
	import FairSite from '$lib/img/fairSite.png';
	import TreeDfolio from '$lib/img/treedfoli.png';
	import ConToTheCrete from '$lib/img/contothecrete.png';
</script>

<header class="head_Line">
	<h1>In progress and Completed work:</h1>
</header>

<svelte:head>
	<title>Lantern Light Development Projects</title>
	<meta
		name="description"
		content="Welcome to the Lantern Light Development Previous Projects Page. "
	/>
	<meta name="keywords" content="web development, web design, software development" />
	<meta property="og:title" content="Lantern Light Development Previous Projects Page" />
	<meta
		property="og:description"
		content="Welcome to the Lantern Light Development Previous Projects Page. "
	/>
	<!-- <meta property="og:image" content="$lib/img/backHero29.png" /> -->
	<meta property="og:url" content="https://www.lanternlightdevelopment.com/" />
	<meta name="twitter:card" content="$lib/img/backHero29.png" />
</svelte:head>

<main class="grid-Main">
	<section>
		<h4>Con to the Crete.com</h4>
		<img src={ConToTheCrete} alt="Con-crete the rapper's project screenshot" />
		<p>
			A friend is a rapper who has created music for years. I made this for him to deal with merch
			sales and tour dates.
		</p>
		<a class="btn-Pulse" href="https://contothecrete.com/">Check it out</a>
	</section>

	<section class="right-Align">
		<h4>3D Portfolio Website</h4>
		<img src={TreeDfolio} alt="3D Portfolio Website project screenshot" />
		<p>
			I spent some time building this websites replacement in 3d. It is fully functioning. There are
			just a few things to work out.
		</p>
		<a class="btn-Pulse" href="https://threedlight.netlify.app/">Check it out</a>
	</section>

	<section>
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

	<section class="right-Align">
		<h4>County Fair</h4>
		<img src={FairSite} alt="Kitsap County Fair project screenshot" />
		<p>
			This is a project I used for getting up to date with different styling updates and data
			techniques.
		</p>
		<a class="btn-Pulse" href="https://newfaircity.netlify.app/">Check it out</a>
		<a class="btn-Pulse" href="/Projects/NewFairCity/">Read about this project</a>
	</section>

	<section>
		<h4>West Sound RD (Full stack)</h4>
		<img src={Wsrd} alt="West Sound RD project screenshot" />
		<p>
			This project marked a big step forward in both complexity and refinement, expanding on
			previous ideas of managing and interacting with website content directly from the page.
		</p>
		<a class="btn-Pulse" href="https://westsoundrd2.netlify.app/">Check it out</a>
		<a class="btn-Pulse" href="/wsrd">Read about this project</a>
	</section>

	<section class="right-Align">
		<h4>3D counter-top store (3D)</h4>
		<img src={ArtCount} alt="3D counter-top store project screenshot" />
		<p>
			I took a course on building 3D websites. This was a way for me to start to understand the
			concepts.
		</p>
		<a class="btn-Pulse" href="https://artisan-countertop-v4.netlify.app/">Check it out</a>
	</section>

	<section class="right-Align">
		<h4>Random Store</h4>
		<img src={RandShop} alt="Random store website screenshot" />
		<p>I built this page to learn about making an online storefront.</p>
		<a class="btn-Pulse" href="https://sky-high-shop-test.netlify.app/">Check it out</a>
	</section>
</main>

<style>
	section {
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
</style>
