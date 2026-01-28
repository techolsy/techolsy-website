<script>
  import Gitcard from '$lib/components/Gitcard.svelte';
</script>

<svelte:head>
  <title>Projects</title>
</svelte:head>

<div class="container flex flex-col mx-auto py-5">
  <h1 class="text-4xl text-center">My Projects</h1>

  <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-4 py-4 mx-auto">
    <Gitcard
      name="Techolsy Website" language="Svelte"
      description="This website, that I build to learn more about svelte"
      url="https://github.com/techolsy/techolsy-website">
    </Gitcard>

    <Gitcard
      name="Ansible" language="Ansible"
      description="This is my personal ansible playbooks that I use for my homelab"
      url="https://github.com/techolsy/ansible">
    </Gitcard>

    <Gitcard
      name="dns-api" language="TypeScript"
      description="dns-api is and api server for dnsmasq to update the hosts file"
      url="https://github.com/techolsy/dns-api">
    </Gitcard>

    <Gitcard
      name="Gitsync" language="Go"
      description="Gitsync is a server configuration tool to sync config from git"
      url="https://github.com/techolsy/gitsync">
    </Gitcard>

    <Gitcard
      name="Lego-wrapper" language="Bash"
      description="Lego-wrapper is a wrapper for the lego acme client"
      url="https://github.com/techolsy/lego-wrapper">
    </Gitcard>

    <Gitcard
      name="encoder" language="TypeScript"
      description="ffmpeg wrapper to encode to hevc using vaapi"
      url="https://github.com/techolsy/encoder">
    </Gitcard>
  </div>
</div>
