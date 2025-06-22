<script>
    // No need to import `goto` since svelte-spa-router doesn't support it directly
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
      z-index: 1000;
      box-sizing: border-box;
      font-family: 'Georgia', serif;
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
    }
  
    .nav-links a:hover {
      text-decoration: underline;
    }
  </style>
  
  <nav>
    <a class="site-title" href="#/">Shanmu Raja</a>
    <div class="nav-links">
      <a href="#/blog">Blog</a>
      <a href="#/publications">Publications</a>
    </div>
  </nav>
  