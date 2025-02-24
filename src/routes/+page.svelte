<script>
  import { onMount } from "svelte";

  let angle = 0;
  let speed = 0.01;
  let time = 0

  function animate() {
    time += speed;
    angle = Math.sin(time) * 5;
    requestAnimationFrame(animate);
  }

  onMount(() => {
    animate();
  });
</script>

<svelte:head>
  <title>Home</title>
  <meta name="Techolsy Home" content="Landing page for techolsy website"/>
</svelte:head>

<div class="flex flex-grow items-center justify-center">
  <h1 class="text-4xl" style="transform: rotate({angle}deg);">Welcome to my website!</h1>
</div>
