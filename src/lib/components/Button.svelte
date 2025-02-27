<script>
  export let name = "Button";
  export let color = "primary";
  export let url = "#"

  const buttonColors = {
    primary: "blue",
    secondary: "red",
    success: "green"
  };
</script>

<div class={`flex py-2 px-2 items-center justify-center border rounded-xl cursor-pointer bg-${buttonColors[color]}-500 hover:bg-${buttonColors[color]}-400 text-white border-gray-200`}>
  <a href="{url}" class="font-semibold">
    {name}
  </a>
</div>
