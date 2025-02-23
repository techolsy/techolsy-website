<script>
  import Header from './Header.svelte';
  import Footer from './Footer.svelte';
  import '../app.css';

  let { children } = $props();
</script>

<div class="flex flex-col min-h-screen bg-gray-800 text-gray-200">
  <header>
    <Header />
  </header>

  <main class="flex flex-grow">
    {@render children()}
  </main>

  <footer class="flex">
    <Footer />
  </footer>
</div>
