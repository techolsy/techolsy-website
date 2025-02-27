<script>
  import Button from "$lib/components/Button.svelte";
</script>

<svelte:head>
  <title>404 - Page Not Found</title>
  <meta name="404 - Page Not Found" content="404 - Page Not Found"> 
</svelte:head>

<div class="flex flex-col flex-grow items-center justify-center">
  <h1 class="text-4xl text-red-500">404 - Page Not Found</h1>
  <p class="text-lg text-gray-400">The page you are looking for does not exist</p>
  <Button 
    name="Go back Home"
    url="/"
    color="primary"/>
</div>
