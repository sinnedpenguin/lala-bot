<script lang="ts">
  import { commands } from "$lib/config/contents";
</script>

<div class="text-center mt-[25vh]" id="commands">
  <h1 class="scroll-m-20 text-4xl font-extrabold tracking-tight lg:text-5xl">
    {commands.header}
  </h1>
  <p class="text-muted-foreground text-lg">
    {commands.subheader}
  </p>
</div>

<section class="container mx-auto flex flex-wrap justify-center gap-4 pb-12 pt-4 mb-[25vh]">
  {#each commands.content as command (command)}
    <div class="flex items-center">
      <code
        class="relative rounded bg-muted px-[0.3rem] py-[0.2rem] font-mono text-sm font-semibold"
      >
        {command}
      </code>
    </div>
  {/each}
</section>