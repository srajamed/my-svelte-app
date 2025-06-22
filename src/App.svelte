<script>
	import Navbar from './Components/Navbar.svelte';
	import Hero from './Components/Hero.svelte';
	import Blog from './Pages/Blog.svelte';
	import Publications from './Pages/Publications.svelte';
	import Router from 'svelte-spa-router';

	const routes = {
		'/': Hero,
		'/blog': Blog,
		'/publications': Publications
	};
</script>

<style>
	:global(html) {
		scroll-behavior: smooth;
	}

	:global(body) {
		margin: 0;
		background-color: #2f3f40;
		color: #f5f5f0;
		font-family: 'Georgia', serif;
	}

	main {
		padding-top: 4.5rem; /* Prevent overlap with fixed navbar */
	}

	/* 🎯 Navigation enhancements */
	.nav-links a {
		transition: color 0.3s ease, text-decoration 0.3s ease;
	}

	.nav-links a:hover {
		text-decoration: underline;
		color: #f6c177;
	}

	.nav-links a.active {
		border-bottom: 2px solid #f6c177;
	}

	/* 🎯 UI Animations: Hover feedback on buttons, posts, etc. */
	button,
	.poster-button,
	.pdf-button,
	.post-entry {
		transition: transform 0.2s ease, box-shadow 0.2s ease;
	}

	button:hover,
	.poster-button:hover,
	.pdf-button:hover,
	.post-entry:hover {
		transform: scale(1.03);
		box-shadow: 0 4px 20px rgba(0, 0, 0, 0.4);
	}

	/* 🎯 Subtle fade-in effect for animated content */
	.fade-in {
		opacity: 0;
		transform: translateY(20px);
		animation: fadeIn 0.8s ease forwards;
	}

	@keyframes fadeIn {
		to {
			opacity: 1;
			transform: translateY(0);
		}
	}
</style>

<Navbar />

<main>
	<Router {routes} />
</main>
