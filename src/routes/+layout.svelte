<script>
  import Header from './Header.svelte';
  import Footer from './Footer.svelte';
  import '@picocss/pico';
  import '../app.css';

  let { children } = $props();
</script>

<div class="app">
  <header class="container">
    <Header />
  </header>

  <hr>

  <main class="container">
    {@render children()}
  </main>

  <footer class="container sticky-footer">
    <Footer />
  </footer>
</div>

<style>
  .app {
    display: flex;
    flex-direction: column;
    min-height: 100vh;
  }

  .sticky-footer {
    margin-top: auto;
  }
</style>
