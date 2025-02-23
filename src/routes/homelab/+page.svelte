<script>
  import Networking from './Networking.svelte';
  import Servers from './Servers.svelte';
  import Services from './Services.svelte';
</script>

<svelte:head>
  <title>Homelab</title>
</svelte:head>

<div class="container mx-auto py-5">
  <h1 class="text-4xl">Homelab</h1>
  <p class="text-xl">Here is my current homelab setup</p>
  <br>
  <Networking />
  <br>
  <Servers />
  <br>
  <Services />
</div>
