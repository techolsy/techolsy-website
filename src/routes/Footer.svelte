<script>
  import SocialIcons from '@rodneylab/svelte-social-icons';

  const mastodonSvg = '/images/mastodon.svg';
</script>

<div class="flex w-full bg-gray-950">
  <div class="flex justify-between container mx-auto py-4">
    <div class="flex items-center justify-center">
      <p class="text-lg text-gray-400">&copy Techolsy 2025</p>
    </div>
    <div class="flex">
      <a href="mailto:alexander@techolsy.eu">
        <SocialIcons alt="" network="email" width="30" height="30" />
      </a>
      <a href="https://linkedin.com/in/alexander-olsson-111b92177" target="_blank" class="ml-2">
        <SocialIcons alt="" network="linkedin" width="30" height="30" />
      </a>
      <a href="https://github.com/techolsy" target="_blank" class="ml-2">
        <SocialIcons alt="" network="github" width="30" height="30" bgColor="#99a1af" />
      </a>
      <a href="https://mastodon.social/@techolsy" target="_blank" class="ml-2">
        <img src="{mastodonSvg}" alt="" height="30" width="30" />
      </a>
    </div>
  </div>
</div>
