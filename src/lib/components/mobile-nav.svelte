<script>
  import { navItems } from "$lib/config/site";
</script>

<header class="w-full border-b bg-background">
  <div class="flex justify-center mt-4">
    <a href="/">
      <nav class="flex items-center">
        <img src="/logo.png" alt="Lalabot" class="sm:h-8 w-8 mr-2" />
      </nav>
    </a>
  </div>
  <div class="container flex h-16 items-center text-center">
    <div class="mt-1 mx-auto">
      {#each navItems as item (item.href)}
        <a href={item.href} class="p-2 text-sm hover:text-gray-500">
          {item.label}
        </a>
      {/each}
    </div>
  </div>
</header>