<script>
  import Navbar from '../Components/Navbar.svelte';

  const posts = [
    {
      title: 'Burnt Red Tongues',
      subtitle: 'They Promised Rice in White Coats',
      date: '05/12/2025',
      link: 'https://medium.com/@shanmuraja/burnt-red-tongues-e5647e67d243',
      image: '/burnt.jpg'
    },
    {
      title: 'The Sound and the Fury',
      subtitle: 'Legacy, Ethics, and the Cost of Progress',
      date: '03/17/2025',
      link: 'https://medium.com/@shanmuraja/the-sound-and-the-fury-b688bde9e526',
      image: '/sound.jpg'
    },
    {
      title: 'Birds Do Not Sing in Caves',
      subtitle: 'Masculinity in Medicine',
      date: '12/28/2024',
      link: 'https://medium.com/@shanmuraja/birds-do-not-sing-in-caves-ef64cb65c790',
      image: '/birds.jpg'
    },
    {
      title: 'Young Boy Blues',
      subtitle: 'My thoughts on caretaking',
      date: '10/21/2024',
      link: 'https://medium.com/hope-healing-and-humour/young-boy-blues-0ce82e7971e0',
      image: '/young.jpg'
    },
    {
      title: "I've Gone to the Country Spa",
      subtitle: 'My reflections on psychiatry and heredity',
      date: '04/12/2024',
      link: 'https://medium.com/hope-healing-and-humour/ive-gone-to-the-country-spa-0b4313d7b8d7',
      image: '/country.jpg'
    },
    {
      title: 'Jack of all Trades, Master of None',
      subtitle: 'My reflection on finding a medical specialty',
      date: '02/25/2024',
      link: 'https://medium.com/@shanmuraja/jack-of-all-trades-master-of-none-3e1be5a35d7b',
      image: '/master.jpg'
    },
    {
      title: 'Sonder',
      subtitle: 'My Time in India',
      date: '11/17/2023',
      link: 'https://medium.com/@shanmuraja/sonder-c07feba361e0',
      image: '/sonder.jpg'
    },
    {
      title: 'Do you lift, bro?',
      subtitle: 'My time in orthopedics',
      date: '09/06/2023',
      link: 'https://medium.com/@shanmuraja/do-you-lift-bro-b2c620677895',
      image: '/lift.jpg'
    },
    {
      title: 'Got Your Toe!',
      subtitle: 'My time in a skilled nursing facility',
      date: '08/09/2023',
      link: 'https://medium.com/@shanmuraja/got-your-toe-472b0e2a74cb',
      image: '/toe.jpg'
    }
  ];
</script>

<style>
  :global(html) {
    scroll-behavior: smooth;
  }

  :global(body) {
    margin: 0;
    background-color: #2f3f40;
    font-family: 'Georgia', serif;
    color: #f5f5f0;
  }

  main {
    padding-top: 5rem;
  }

  .hero {
    position: relative;
    height: 90vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    padding: 2rem;
    overflow: hidden;
  }

  .hero::before {
    content: '';
    position: absolute;
    inset: 0;
    background-image: url('/lift.jpg');
    background-size: cover;
    background-position: center;
    filter: brightness(30%);
    z-index: -1;
  }

  .hero h1 {
    font-size: 4rem;
    font-weight: 500;
    margin-bottom: 1rem;
    color: white;
    position: relative;
  }

  .post-entry {
    max-width: 800px;
    margin: 4rem auto;
    padding: 0 1rem;
    text-align: center;
    transition: transform 0.3s ease;
  }

  .post-entry:hover {
    transform: scale(1.02);
  }

  .post-entry img {
    width: 100%;
    max-width: 550px;
    height: auto;
    aspect-ratio: 4 / 3;
    object-fit: cover;
    border-radius: 6px;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.3);
  }

  .post-date {
    margin-top: 1.25rem;
    font-size: 0.9rem;
    color: #bbb;
  }

  .post-title {
    font-size: 2rem;
    margin: 0.5rem 0;
    color: #f5f5f0;
  }

  .post-subtitle {
    font-size: 1.15rem;
    color: #ccc;
    font-weight: 400;
  }

  a.post-link {
    text-decoration: none;
    color: inherit;
  }

  footer {
    padding: 4rem 2rem 3rem;
    text-align: center;
    color: #999;
    font-size: 0.9rem;
  }

  @media (max-width: 600px) {
    .hero h1 {
      font-size: 2.5rem;
    }

    .post-title {
      font-size: 1.5rem;
    }

    .post-subtitle {
      font-size: 1rem;
    }

    .post-entry img {
      width: 100%;
      height: auto;
    }

    .post-entry {
      padding: 0 0.5rem;
    }

    footer {
      font-size: 0.8rem;
    }
  }
</style>

<Navbar />

<main>
  <section class="hero">
    <h1>Stories in Medicine</h1>
  </section>

  {#each posts as post}
    <a href={post.link} target="_blank" rel="noopener" class="post-link">
      <div class="post-entry">
        <img src={post.image} alt={post.title} />
        <div class="post-date">{post.date}</div>
        <div class="post-title">{post.title}</div>
        <div class="post-subtitle">{post.subtitle}</div>
      </div>
    </a>
  {/each}
</main>

<footer>
  &copy; {new Date().getFullYear()} Shanmu Raja — All rights reserved.
</footer>
