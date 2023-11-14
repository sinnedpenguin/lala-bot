<script lang="ts">
  import { termsOfService } from "$lib/config/contents";
</script>

<section class="container mx-auto flex flex-col gap-4 pb-12 pt-4 lg:gap-8">
  <h1 class="scroll-m-20 text-4xl font-extrabold tracking-tight lg:text-5xl text-center">
    {termsOfService.header}
  </h1>

  {#each termsOfService.content as term (term.title)}
    <div class="max-w-2xl mx-auto">
      <h3 class="scroll-m-20 text-2xl font-bold tracking-tight">{term.title}</h3>
      <p>{term.description}</p>
    </div>
  {/each}
</section>