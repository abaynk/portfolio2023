<script lang="ts">
  export let active = '';
  export let y = 0;

  $: active = y >= 500 ? 'exp' : 'about';

  $: console.log({ active });
  $: console.log({ y });
</script>

<div class="main">
  <div class="main-content">
    <h1>Abay Nurpeissov</h1>
    <h2>Frontend developer</h2>
    <p class="main-content__paragraph">
      Through constant self-improvement and learning I bring amazing ideas to
      life
    </p>
  </div>
  <div class="main-nav">
    <a on:click={() => (active = 'about')} href="#about">
      <h4 class="link" class:active={active === 'about'}>ABOUT</h4>
    </a>
    <a on:click={() => (active = 'exp')} href="#exp">
      <h4 class="link" class:active={active === 'exp'}>EXPERIENCE</h4>
    </a>
  </div>
  <div class="main-links">
    <a href="https://github.com/abaynk" target="_blank" rel="noreferrer"
      ><img class="icon" src="github.svg" alt="gh" /></a
    >
    <a
      href="https://www.linkedin.com/in/abay-nurpeissov-1a44a0192/"
      target="_blank"
      rel="noreferrer"><img class="icon" src="linkedin.svg" alt="in" /></a
    >
    <a href="mailto: abaynk123@gmail.com" target="_blank" rel="noreferrer"
      ><img class="icon" src="mail.svg" alt="gm" /></a
    >
    <a
      href="https://www.instagram.com/qoblanuly/"
      target="_blank"
      rel="noreferrer"><img class="icon" src="instagram.svg" alt="ig" /></a
    >
    <a
      href="https://www.youtube.com/@abaynurpeissov8936"
      target="_blank"
      rel="noreferrer"><img class="icon" src="youtube.svg" alt="yt" /></a
    >
  </div>
</div>

<style lang="scss">
  .main {
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }
  .main-nav {
    display: flex;
    flex-direction: column;
    row-gap: 20px;
    & > a {
      max-width: fit-content;
    }
  }
  .link {
    position: relative;
    max-width: fit-content;
    text-align: left;
    opacity: 0.6;
    cursor: pointer;
    transition: 0.5s;
    &:hover {
      padding: 0 110px;
      opacity: 1;
      &::before {
        content: ' ';
        display: block;
        height: 1px;
        width: 100px !important;
        position: absolute;
        top: 50%;
        left: 0;
        background: #e0e1dd;
      }
    }
  }
  .link::before {
    content: '';
    display: block;
    height: 1px;
    width: 100px;
    position: absolute;
    top: 50%;
    left: 0;
    background: #e0e1dd;
  }
  .active {
    padding: 0 110px;
    opacity: 1;
  }
  .active::before {
    content: '';
    display: block;
    height: 1px;
    width: 100px !important;
    position: absolute;
    top: 50%;
    left: 0;
    background: #e0e1dd;
  }
  .main-links {
    display: flex;
    column-gap: 20px;
  }
  .icon {
    cursor: pointer;
    filter: invert(98%) sepia(7%) saturate(88%) hue-rotate(26deg)
      brightness(95%) contrast(87%);
    opacity: 0.6;
  }
  .icon:hover {
    opacity: 1;
  }
  .main-content__paragraph {
    width: 80%;
  }

  @media (max-width: 1023px) {
    .main {
      row-gap: 50px;
    }
    .main-nav {
      display: none;
    }
  }
  @media (max-width: 480px) {
    .main-content__paragraph {
      width: 100%;
    }
  }
</style>
