<script>
  import { Handle } from "@xyflow/svelte";
  export let data;
</script>

<div class="flex bg-gray-900 shadow-lg rounded-lg border border-gray-400 w-38 h-9">
  <Handle type="target" position="top" />
  <div class="flex flex-grow text-gray-200 items-center justify-center">{data.label}</div>
  <Handle type="source" position="bottom" />
</div>
