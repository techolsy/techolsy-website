<script>
  import { page } from "$app/stores";

  const sitePages = ['Home', 'About', 'Projects','Homelab'];
  const menuClass = "text-lg no-underline hover:text-blue-500 ml-3";
  const menuActive = "text-lg no-underline text-blue-400 hover:text-blue-500 ml-3";
</script>
<div class="w-full bg-gray-700">
  <div class="container mx-auto">
    <nav class="flex flex-col text-center sm:flex-row sm:text-left sm:justify-between py-4 sm:items-baseline w-full">
      <div class="mb-2 sm:mb-0">
        <a href="/" class="text-2xl no-underline text-gray-200 hover:text-blue-300">Techolsy</a>
      </div>
      <div>
        {#each sitePages as sitePage}
          {#if sitePage === 'Home'}
            <a href="/" class="{$page.url.pathname === '/' ? menuActive : menuClass}">{sitePage}</a>
          {:else}
            <a href={"/" + sitePage.toLowerCase()} class="{$page.url.pathname === '/' + sitePage.toLowerCase() ? menuActive : menuClass}">{sitePage}</a>
          {/if}
        {/each}
      </div>
    </nav>
  </div>
</div>
