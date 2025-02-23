<script>
  export let error = { status: 404};
</script>

<svelte:head>
  <title>{error.status === 404 ? 'Page Not Found' : 'Error'}</title>
</svelte:head>

<main class="flex flex-grow items-center justify-center">
  <div class="max-w-96">
  <h1 class="text-4xl text-red-700">{error.status === 404 ? '404 - Page Not Found' : 'An Error Occurred'}</h1>
  <p class="text-lg">{error.message || 'Sorry the page you are looking for does not exist'}</p>
  <a href="/" class="text-yellow-400 hover:text-blue-200 underline">Go back home</a>
</div>
</main>
