<script>
  import ExpBlock from './ExpBlock.svelte';
</script>

<h4 class="heading">EXPERIENCE</h4>
<div class="scroll-container">
  <ExpBlock
    link="https://www.linkedin.com/company/adastra.one/"
    period="Jan 2022 - present"
    company="ADASTRA·ONE"
    position="JavaScript developer"
    location="remote"
    description="significantly improved usability, reduced data loading time, enhanced the debugging process, and increased efficiency, resulting in a better performance and user experience for the browser-extension."
    skills={[
      'TypeScript',
      'Svelte',
      'Sass',
      'HTML5',
      'JavaScript',
      'Git',
      ' npm',
    ]}
  />
  <ExpBlock
    link="https://www.linkedin.com/company/boc-products-and-services-ag/"
    period="Sep 2021 - Dec 2021"
    company="BOC Group"
    position="Software engineering intern"
    location="Vienna, Austria"
    description="• Researched image recognition<br/>• Implemented OpenCV scripts in webapp"
    skills={['OpenCV', 'JavaScript']}
  />
  <ExpBlock
    link="https://www.linkedin.com/company/vedom/"
    period="Apr 2021 - Sep 2021"
    company="VEDOM"
    position="Frontend developer"
    location="remote"
    description="• Built front end of a marketplace web app in a close collaboration with UX and Back end teams<br/>• Increased usability of web app by extending components library by 500% and implementing cross platform responsiveness<br/>• Optimized page loading time by 150% and decreased memory usage by 170% by implementing image caching and lazy loading<br/>• Supported back end team on maintaining REST APIs, fixed 25% of API request by configuring CORS and serverless functions"
    skills={[
      'React',
      'Google Analytics',
      'i18n',
      'AWS',
      'Node.js',
      'Sass',
      'JavaScript',
      'Git',
      'HTML',
    ]}
  />
</div>

<style lang="scss">
  .heading {
    padding-left: 20px;
    margin-bottom: 20px;
  }
  .scroll-container {
    display: flex;
    flex-direction: column;
    row-gap: 20px;
  }
  @media (max-width: 1023px) {
    .heading {
      padding-left: 0px;
    }
  }
</style>
