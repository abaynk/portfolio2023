<script lang="ts">
  export let link: string = '';
  export let period: string = 'date - date';
  export let company: string = 'Company';
  export let position: string = 'Position';
  export let location: string = 'location';
  export let description: string = 'Description';
  export let skills: string[] = ['Skills', 'Skills', 'Skills', 'Skills'];
</script>

<a href={link} target="_blank" rel="noreferrer">
  <div class="root">
    <div class="date">
      <p>{period}</p>
      <p class="location">{location}</p>
    </div>
    <div class="root-content">
      <p class="company">{company}</p>
      <p class="position">{position}</p>
      <p class="description">{@html description}</p>
      <div class="skills">
        {#each skills as skill}
          <p class="skill">{skill}</p>
        {/each}
      </div>
    </div>
  </div>
</a>

<style lang="scss">
  .root {
    display: flex;
    align-items: start;
    column-gap: 20px;
    padding: 20px;
  }
  .root-content {
    max-width: calc(100% - 220px);
  }
  .root:hover {
    background: rgba(255, 255, 255, 0.05);
    box-shadow: 0 8px 32px 0 rgba(31, 38, 135, 0.37);
    backdrop-filter: blur(1px);
    -webkit-backdrop-filter: blur(1px);
    border-radius: 10px;
    cursor: pointer;
    transition: 0.3s ease-in-out;
    & > .root-content > .company {
      transition: 0.3s ease-in-out;
      color: #778da9;
    }
  }

  .company {
    opacity: 1;
  }
  .description {
    font-size: 16px;
    margin-top: 10px;
  }

  .date,
  .position,
  .location {
    opacity: 0.4;
  }
  .date {
    min-width: 160px;
  }
  .skills {
    margin-top: 10px;
    display: flex;
    column-gap: 5px;
    row-gap: 5px;
    flex-wrap: wrap;
  }
  .skill {
    background-color: #415a77;
    padding: 0px 10px;
    font-size: 16px;
    border-radius: 50px;
    opacity: 1;
  }
  @media (max-width: 1023px) {
    .root {
      padding-left: 0px;
      pointer-events: none;
    }
  }
</style>
