<script>
  export let title = "Card title";
  export let link = "link"
</script>

<div class="p-4">
  <div class="border border-gray-400 rounded-lg overflow-hidden max-w-96">
    <div class="bg-gray-600 w-full p-4">
      <a href="{link}" target="_blank">
        <h3 class="text-lg fond-semibold text-gray-900 text-center">{title}</h3>
      </a>
    </div>
    <div class="max-auto p-4 overflow-hidden">
      <slot>
      </slot>
    </div>
  </div>
</div>
