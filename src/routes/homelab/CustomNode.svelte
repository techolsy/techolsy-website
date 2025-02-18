<script>
  import { Handle } from "@xyflow/svelte";
  export let data;
</script>

<div class="custom-node">
  <Handle type="target" position="top" />
  <div>{data.label}</div>
  <Handle type="source" position="bottom" />
</div>

<style>
  .custom-node {
    padding: 10px;
    background: white;
    border-radius: 5px;
    text-align: center;
    border: 1px solid #ccc;
  }

  :global(.svelte-flow__handle) {
    width: 6px !important;
    height: 6px !important;
    background-color: #007bff !important;
    border-radius: 50% !important;
    border: none !important;
    padding: 0 !important;
    margin: 0 !important;
    box-shadow: none !important;
    display: block !important;
  }
</style>
