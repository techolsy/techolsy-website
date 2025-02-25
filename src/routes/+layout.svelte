<script>
  import Header from './Header.svelte';
  import Footer from './Footer.svelte';
  import '../app.css';

  let { children } = $props();
</script>

<div class="flex flex-col min-h-screen bg-gray-900 text-gray-100">
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
