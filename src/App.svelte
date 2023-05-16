<script lang="ts">
  import Content from './components/Content.svelte';
  import MainInfo from './components/MainInfo.svelte';

  let active = 'about';
  let y: number = 0;
</script>

<svelte:window bind:scrollY={y} />

<header class="container mainInfo">
  <MainInfo bind:active bind:y />
</header>

<main>
  <div class="root">
    <div class="container content"><Content bind:active bind:y /></div>
  </div>
</main>

<style>
  .mainInfo {
    position: fixed;
    top: 6rem;
    padding-left: 6rem;
    height: calc(100% - 12rem);
  }
  .root {
    height: 100vh;
    padding: 6rem;
    padding-left: 50%;
  }

  @media (max-width: 1023px) {
    .mainInfo {
      position: relative;
      height: fit-content;
      top: 0;
      padding: 3rem;
      padding-bottom: 0;
    }
    .root {
      height: 100vh;
      padding: 3rem;
    }
  }
  @media (max-width: 480px) {
    .mainInfo {
      padding: 1rem;
    }
    .root {
      padding: 1rem;
    }
  }
</style>
