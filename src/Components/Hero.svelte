<style>
  .hero {
    background-image: linear-gradient(
        rgba(0, 0, 0, 0.3),
        rgba(0, 0, 0, 0.3)
      ),
      url('/hero-bg.jpg');
    background-size: cover;
    background-position: center;
    color: #f5f5f0;
    padding: 8rem 2rem 4rem;
    text-align: center;
    font-family: 'Inter', sans-serif;
    width: 100%;
    box-sizing: border-box;
  }

  .hero h1 {
    font-size: 2rem;
    line-height: 1.6;
    max-width: 900px;
    margin: 0 auto;
  }

  .about-wrapper {
    background-color: #2f3f40;
    padding: 4rem 0;
    width: 100%;
    box-sizing: border-box;
  }

  .about-container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 2rem;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    gap: 3rem;
    align-items: center;
    color: #f5f5f0;
    font-family: 'Inter', sans-serif;
  }

  .about-text {
    flex: 1;
    font-size: 1.1rem;
    line-height: 1.6;
  }

  .about-text p {
    margin-bottom: 1rem;
  }

  .about-img {
    flex: 1;
    display: flex;
    justify-content: center;
  }

  .about-img img {
    width: 100%;
    max-width: 500px;
    border-radius: 0.5rem;
  }

  .social-icons {
    margin-top: 1.5rem;
    display: flex;
    gap: 1.5rem;
    align-items: center;
    flex-wrap: wrap;
    justify-content: center;
  }

  .social-icons a {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    padding: 0.4rem;
    background-color: rgba(255, 255, 255, 0.07);
    border-radius: 50%;
    transition: transform 0.2s ease, background-color 0.2s ease;
  }

  .social-icons a:hover {
    background-color: rgba(255, 255, 255, 0.15);
    transform: scale(1.1);
  }

  .social-icons img {
    width: 28px;
    height: 28px;
    filter: brightness(0) invert(1);
    opacity: 0.95;
    transition: transform 0.2s ease;
  }

  :global(body) {
    margin: 0;
    overflow-x: hidden;
  }

  /* 📱 Mobile Optimization */
  @media (max-width: 768px) {
    .hero {
      padding: 6rem 1rem 3rem;
    }

    .hero h1 {
      font-size: 1.5rem;
      padding: 0 1rem;
    }

    .about-container {
      flex-direction: column-reverse;
      gap: 2rem;
      text-align: center;
      padding: 0 1.2rem;
    }

    .about-text {
      font-size: 1rem;
    }

    .about-img img {
      max-width: 90%;
    }
  }
</style>

<!-- HERO SECTION -->
<section class="hero">
  <h1>
    I'm an aspiring medical student. Graduate from Boston University and UCSF. My interests include<br />
    surgical research, healthcare economics/policy,<br />
    and creative medical writing.
  </h1>
</section>

<!-- ABOUT SECTION -->
<section class="about-wrapper">
  <div class="about-container">
    <div class="about-text">
      <p>
        I’m based in California. I spend my free time writing, playing squash,
        practicing piano, cooking, and watching movies.
      </p>
      <p>The best ways to get in touch:</p>
      <p><strong>shanmur@uclawsf.edu</strong></p>

      <div class="social-icons">
        <a href="https://shanmuraja.medium.com" target="_blank" rel="noopener">
          <img src="/medium-icon.svg" alt="Medium" />
        </a>
        <a href="https://www.instagram.com/shanmuraja_" target="_blank" rel="noopener">
          <img src="/instagram-icon.svg" alt="Instagram" />
        </a>
        <a href="https://twitter.com/shanmugeshraja" target="_blank" rel="noopener">
          <img src="/x-icon.svg" alt="X/Twitter" />
        </a>
        <a href="https://www.linkedin.com/in/shanmuraja" target="_blank" rel="noopener">
          <img src="/link-icon.svg" alt="LinkedIn" />
        </a>
      </div>
    </div>

    <div class="about-img">
      <img src="/portrait.jpg" alt="Shanmu Raja" />
    </div>
  </div>
</section>
