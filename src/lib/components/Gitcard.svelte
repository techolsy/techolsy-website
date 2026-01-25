<script>
  export let name = "Repository Name";
  export let description = "A short description of the project.";
  export let language = "JavaScript";
  export let url = "#";

  const languageColors = {
    JavaScript: "bg-yellow-500",
    TypeScript: "bg-blue-500",
    Python: "bg-green-500",
    Rust: "bg-orange-500",
    Go: "bg-blue-600",
    Bash: "bg-green-700",
    Svelte: "bg-[#ff3e00]",
    Ansible: "bg-red-600",
    default: "bg-gray-500"
  };
</script>

<div class="bg-gray-800 shadow-lg rounded-2xl p-5 border border-gray-300 w-80">
  <h2 class="text-xl font-bold text-gray-200 truncate">{name}</h2>
  <p class="text-gray-300 text-sm mt-2 line-clamp-2">{description}</p>

  <div class="flex items-center justify-between mt-4">
    <span class={`text-xs text-white px-2 py-1 rounded ${languageColors[language] || languageColors.default}`}>
      {language}
    </span>
  </div>

  <a href={url} target="_blank" class="mt-4 block text-center bg-blue-500 text-white text-sm font-semibold py-2 rounded-lg hover:bg-blue-600 transition">
    View on GitHub
  </a>
</div>
