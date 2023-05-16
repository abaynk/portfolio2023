<script lang="ts">
  import About from './About.svelte';
  import Experience from './Experience.svelte';
</script>

<div class="content">
  <div class="content-section about" id="about">
    <About />
  </div>
  <div class="content-section exp" id="exp"><Experience /></div>
  <div class="content-section credits" id="projects">
    <h4>Credits</h4>
    <p>
      Design inspired by <a
        href="https://brittanychiang.com/"
        target="_blank"
        rel="noreferrer"
        class="link">Brittany Chiang</a
      >, coded during the warm Anatolian night :) Built with
      <a
        href="https://svelte.dev/"
        target="_blank"
        rel="noreferrer"
        class="link">Svelte</a
      >
      and
      <a
        href="https://sass-lang.com/guide"
        target="_blank"
        rel="noreferrer"
        class="link">SASS</a
      >

      , deployed with
      <a
        href="https://vercel.com/dashboard"
        target="_blank"
        rel="noreferrer"
        class="link">Vercel</a
      >.
    </p>
  </div>
</div>

<style lang="scss">
  .content {
    height: fit-content;
    display: flex;
    flex-direction: column;
    row-gap: 9rem;
  }
  .content-section {
    scroll-margin-top: 6rem !important;
  }

  .about {
    padding-left: 20px;
  }
  .credits {
    padding-bottom: 6rem;
    padding-left: 20px;
    & > h4 {
      margin-bottom: 20px;
    }
  }
  .link {
    color: #778da9;
    opacity: 1;
    &:hover {
      text-decoration: underline;
    }
  }
  @media (max-width: 1023px) {
    .about {
      padding-left: 0px;
    }
  }
  @media (max-width: 480px) {
    .content {
      row-gap: 1rem;
    }
    .credits {
      padding: 0;
      padding-bottom: 1rem;
    }
  }
</style>
