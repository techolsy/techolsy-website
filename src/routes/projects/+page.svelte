<script>
  import Card from '$lib/components/Card.svelte';
</script>

<svelte:head>
  <title>Projects</title>
</svelte:head>

<div class="container flex flex-col mx-auto py-5">
  <h1 class="text-4xl text-center">My Projects</h1>

  <div class="flex p-4 mx-auto">
    <Card title="Gitsync" link="https://github.com/techolsy/gitsync">
      <p>Gitsync is a project written in Go to sync server configuration from a git repository</p>
    </Card>

    <Card title="Lego-wrapper" link="https://github.com/techolsy/lego-wrapper">
      <p>
        Lego-wrapper is shell script wrapper written in bash for the lego acme client, that is used to 
        obtain and renew certificate from an acme server.
      </p>
    </Card>

    <Card title="DNS-API" link="https://github.com/techolsy/dns-api">
      <p>
        DNS-API is and api written in typescript using deno and hono, it is used to updated /etc/hosts used
        by dnsmasq
      </p>
    </Card>
  </div>
</div>
