<script lang="ts">
  import { navItems } from "$lib/config/site";
</script>

<header class="w-full border-b bg-background">
  <div class="container flex h-16 items-center justify-between">
    <div class="flex items-center">
      <a href="/">
        <nav class="flex items-center">
          <img src="/logo.png" alt="Lalabot" class="sm:h-8 w-8 mr-2" /> <span class="font-bold sm:inline text-primary">Lalabot</span>
        </nav>
      </a>
    </div>
    <div class="flex items-center">
      {#each navItems as item (item.href)}
        <a href={item.href} class="ml-4 text-sm hover:text-gray-500">
          {item.label}
        </a>
      {/each}
    </div>
  </div>
</header>