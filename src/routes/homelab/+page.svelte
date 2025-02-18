<script>
  import Networking from './Networking.svelte';
  import Servers from './Servers.svelte';
  import Services from './Services.svelte';
</script>

<svelte:head>
  <title>Homelab</title>
</svelte:head>

<h1>Homelab</h1>
<p>Here is my current homelab setup</p>

<Networking />
<Servers />
<Services />
