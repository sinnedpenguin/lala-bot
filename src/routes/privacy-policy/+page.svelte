<script lang="ts">
  import { privacyPolicy } from "$lib/config/contents";
</script>

<section class="container mx-auto flex flex-col gap-4 pb-12 pt-4 lg:gap-8 mb-[15vh]">
  <h1 class="scroll-m-20 text-4xl font-extrabold tracking-tight lg:text-5xl text-center">
    {privacyPolicy.header}
  </h1>

  {#each privacyPolicy.content as policy (policy.title)}
    <div class="max-w-2xl mx-auto">
      <h3 class="scroll-m-20 text-2xl font-bold tracking-tight">{policy.title}</h3>
      <p>{policy.description}</p>
    </div>
  {/each}
</section>