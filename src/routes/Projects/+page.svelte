<script>
	import Wsrd from '$lib/img/wsrd.png';
	import ArtCount from '$lib/img/artCountV4.png';
	import RandReci from '$lib/img/food.png';
	import RandShop from '$lib/img/shoppo.png';
	import FairSite from '$lib/img/fairSite.png';
	import TreeDfolio from '$lib/img/treedfoli.png';
</script>

<header class="head_Line">
	<h1>In progress / Completed work:</h1>
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

	<section class="right-Align">
		<img src={Wsrd} alt="West Sound RD project screenshot" />
		<h3>West Sound RD (Full stack)</h3>
		<p>
			This project marked a big step forward in both complexity and refinement, expanding on
			previous ideas of managing and interacting with website content directly from the page.
		</p>
		<a class="pulse-button" href="https://westsoundrd2.netlify.app/">Check it out</a>
		<a class="pulse-button" href="/reviews/wsrd">Read about this project</a>
	</section>

	<section>
		<img src={ArtCount} alt="3D counter-top store project screenshot" />
		<h3>3D counter-top store (3D)</h3>
		<p>
			I took a course on building 3D websites. This was a way for me to start to understand the
			concepts.
		</p>
		<a class="pulse-button" href="https://artisan-countertop-v4.netlify.app/">Check it out</a>
	</section>

	<section class="right-Align">
		<img src={RandShop} alt="Random store website screenshot" />
		<h3>Random Store</h3>
		<p>I built this page to learn about making an online storefront.</p>
		<a class="pulse-button" href="https://sky-high-shop-test.netlify.app/">Check it out</a>
	</section>
</main>

<!--svelte-ignore css_unused_selector -->
