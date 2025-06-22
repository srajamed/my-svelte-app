<script>
  let openSection = null;

  function toggle(section) {
    openSection = openSection === section ? null : section;
  }
</script>

<style>
  :global(html) {
    scroll-behavior: smooth;
  }

  :global(body) {
    margin: 0;
    background-color: #2f3f40;
  }

  main {
    color: #f5f5f0;
    font-family: 'Georgia', serif;
    max-width: 1000px;
    margin: 0 auto;
    padding: 6rem 2rem 3rem;
  }

  h1 {
    text-align: center;
    font-size: 2.75rem;
    margin-bottom: 3rem;
    position: relative;
  }

  h1::after {
    content: '';
    width: 100px;
    height: 4px;
    background-color: #f6c177;
    display: block;
    margin: 0.5rem auto 0;
    border-radius: 4px;
  }

  .section-button {
    background: none;
    border: none;
    width: 100%;
    text-align: left;
    padding: 1.25rem 0;
    color: #f5f5f0;
    font-size: 1.8rem;
    font-family: inherit;
    font-weight: bold;
    display: flex;
    justify-content: space-between;
    align-items: center;
    cursor: pointer;
    transition: background-color 0.3s ease;
  }

  .section-button:hover {
    background-color: rgba(255, 255, 255, 0.05);
  }

  .chevron {
    font-size: 1.4rem;
    transition: transform 0.3s ease;
  }

  .rotate {
    transform: rotate(180deg);
  }

  .content {
    overflow: hidden;
    max-height: 0;
    transition: max-height 0.5s ease;
  }

  .content.open {
    max-height: 1000px;
    transition: max-height 0.75s ease;
  }

  .paper {
    margin: 1.25rem 0;
    font-size: 1.1rem;
    line-height: 1.6;
  }

  .paper strong {
    display: block;
    margin-bottom: 0.35rem;
  }

  .pdf-button {
    display: inline-block;
    margin-top: 1rem;
    margin-right: 1rem;
    padding: 0.75rem 1.4rem;
    background-color: #f6c177;
    color: #2f3f40;
    border: none;
    border-radius: 6px;
    font-weight: bold;
    font-family: inherit;
    text-decoration: none;
    transition: background-color 0.3s ease, transform 0.2s ease;
    font-size: 1rem;
  }

  .pdf-button:hover {
    background-color: #e3a65c;
    transform: scale(1.05);
  }

  footer {
    padding: 4rem 2rem 3rem;
    text-align: center;
    color: #999;
    font-size: 0.9rem;
  }
</style>

<main>
  <h1>Publications</h1>

  <!-- Section: Working Papers -->
  <button class="section-button" on:click={() => toggle('working')}>
    Working Papers
    <span class="chevron" class:rotate={openSection === 'working'}>⌃</span>
  </button>
  <div class="content" class:open={openSection === 'working'}>
    <div class="paper">
      <strong>“Variation of Reimbursements within DRGs in Orthopedic Trauma”</strong>
      Shanmugesh Raja, John Wixted  
      <br />Healthcare Economics and Policy
      <br /><span>📝 Working Paper</span>
    </div>
    <div class="paper">
      <strong>“Pathomorphological Characterization of Type B Aortic Dissection Helicity and Influence of Renovisceral Branches”</strong>
      Johann Bondesson, Shanmugesh Raja, Ga-Young Suh, Brant Ullery, Michael Drake, Jason Lee, Christopher Cheng
      <br /><span>📝 Working Paper</span>
    </div>
  </div>

  <!-- Section: Remodeling -->
  <button class="section-button" on:click={() => toggle('remodeling')}>
    Geometric Analysis of Aortic Remodeling
    <span class="chevron" class:rotate={openSection === 'remodeling'}>⌃</span>
  </button>
  <div class="content" class:open={openSection === 'remodeling'}>
    <div class="paper">
      <strong>
        Ullery, B. W., Suh, G.-Y., Bondesson, J., Raja, S., & Cheng, C. (2024).<br />
        Geometric Analysis of Aortic Remodeling After PETTICOAT Technique in Type B Aortic Dissection.
      </strong>
      <em>Journal of Vascular Surgery, 79(6), e149–e150.</em><br />
      <a
        href="https://doi.org/10.1016/j.jvs.2024.03.183"
        target="_blank"
        class="pdf-button"
      >
        📄 View DOI
      </a>
      <a
        href="https://www.jvascsurg.org/article/S0741-5214(24)00670-0/pdf"
        target="_blank"
        class="pdf-button"
      >
        📄 View PDF
      </a>
    </div>
  </div>

  <!-- Section: True Lumen -->
  <button class="section-button" on:click={() => toggle('lumen')}>
    Longitudinal Mapping of True Lumen Morphology
    <span class="chevron" class:rotate={openSection === 'lumen'}>⌃</span>
  </button>
  <div class="content" class:open={openSection === 'lumen'}>
    <div class="paper">
      Longitudinal Mapping of True Lumen Morphology for Accurate Endograft Oversizing in Patients with Type B Aortic Dissections  
      Bondesson, Johan et al.  
      <br />Journal of Vascular Surgery, Volume 77, Issue 4, 64S - 65S
      <br />
      <a
        href="https://www.jvascsurg.org/action/showPdf?pii=S0741-5214%2823%2900233-1"
        target="_blank"
        class="pdf-button"
      >
        📄 View PDF
      </a>
    </div>
  </div>

  <!-- Section: Poster -->
  <button class="section-button" on:click={() => toggle('poster')}>
    Annual Vascular Meeting 2024
    <span class="chevron" class:rotate={openSection === 'poster'}>⌃</span>
  </button>
  <div class="content" class:open={openSection === 'poster'}>
    <a
      href="https://drive.google.com/file/d/1i1kCSeEkCI7UrBNCV-90qE9kBPo0675r/view"
      target="_blank"
      rel="noopener"
      class="pdf-button"
    >
      📄 View Poster
    </a>
  </div>
</main>

<footer>
  &copy; {new Date().getFullYear()} Shanmu Raja — All rights reserved.
</footer>
