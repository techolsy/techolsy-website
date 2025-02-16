<script>
  const site_pages = ['Home', 'About'];
</script>

<nav>
  <ul>
    <li><strong>Techolsy</strong></li>
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
