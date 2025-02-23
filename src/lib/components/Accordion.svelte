<script>
  export let title = "Accordion Title";
  let isOpen = false;
</script>

<div class="border border-gray-400 rounded-lg overflow-hidden">
  <button class="w-full flex justify-between items-center bg-gray-700 p-4 text-left cursor-pointer" on:click={() => isOpen = !isOpen}>
    <span class="font-semibold">{ title }</span>
    <span class="transition-transform transform {isOpen ? 'rotate-180' : 'rotate-0'}">▼</span>
  </button>

  <div class={`transition-all duration-300 ${isOpen ? "max-auto p-4" : "max-h-0 overflow-hidden p-0"}`}>
    <slot></slot>
  </div>
</div>
