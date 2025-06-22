<script>
  import { onMount } from 'svelte';

  let scrolled = false;

  onMount(() => {
    const handleScroll = () => {
      scrolled = window.scrollY > 50;
    };

    window.addEventListener('scroll', handleScroll);
    handleScroll();

    return () => window.removeEventListener('scroll', handleScroll);
  });
</script>

<style>
  nav {
    position: fixed;
    top: 0;
    width: 100%;
    padding: 1.5rem 2rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
    background-color: transparent;
    transition: background-color 0.3s ease, box-shadow 0.3s ease, backdrop-filter 0.3s ease;
    z-index: 1000;
    box-sizing: border-box;
    font-family: 'Georgia', serif;
  }

  nav.scrolled {
    background-color: rgba(18, 18, 18, 0.40);
    box-shadow: 0 2px 12px rgba(0, 0, 0, 0.35);
    backdrop-filter: blur(6px);
  }

  .site-title {
    font-size: 1.9rem;
    font-weight: bold;
    text-decoration: none;
    color: #ffffff;
    opacity: 1;
    transition: opacity 0.3s ease;
  }

  .site-title:hover {
    opacity: 0.85;
  }

  .nav-links {
    display: flex;
    align-items: center;
  }

  .nav-links a {
    margin-left: 2rem;
    text-decoration: none;
    font-size: 1.35rem;
    font-weight: 500;
    color: #f5f5f0;
    font-family: 'Inter', sans-serif;
    letter-spacing: 0.5px;
    transition: color 0.3s ease;
  }

  .nav-links a:hover {
    text-decoration: underline;
    color: #f6c177;
  }
</style>

<nav class:scrolled={scrolled}>
  <a class="site-title" href="#/">Shanmu Raja</a>
  <div class="nav-links">
    <a href="#/blog">Blog</a>
    <a href="#/publications">Publications</a>
  </div>
</nav>
