<script>
  import '@fortawesome/fontawesome-free/css/all.min.css'

  const site_pages = ['Home', 'About', 'Homelab'];
</script>

<nav>
  <ul>
    <li><strong>Techolsy</strong></li>
    <li>
      <a href="https://github.com/techolsy" target="_blank" aria-labelledby="github">
        <i class="fa-brands fa-square-github fa-xl icon"></i>
      </a>
    </li>
    <li>
      <a href="https://linkedin.com/in/alexander-olsson-111b92177" target="_blank" aria-labelledby="linkedin">
        <i class="fa-brands fa-linkedin fa-xl icon"></i>
      </a>
    </li>
  </ul>
    <ul>
    {#each site_pages as site_page}
      <li>
        {#if site_page === 'Home'}
          <a href="/" class="contrast">{site_page}</a>
        {:else}
          <a href="/{site_page.toLowerCase()}" class="contrast">{site_page}</a>
        {/if}
      </li>
    {/each}
  </ul>
</nav>

<style>
  .icon {
    color: #77767b;
  }
</style>
