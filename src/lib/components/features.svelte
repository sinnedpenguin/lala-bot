<script lang="ts">
  import { features } from "$lib/config/contents";
</script>

<div class="text-center" id="features">
  <h1 class="scroll-m-20 text-4xl font-extrabold tracking-tight lg:text-5xl">
    {features.header}
  </h1>
  <p class="text-muted-foreground text-lg">
    {features.subheader}
  </p>
</div>

<section class="container mx-auto grid grid-cols-1 gap-4 pb-12 pt-4 lg:grid-cols-2 lg:gap-8">
  <div class="text-center lg:text-left"> 
    {#each features.content as feature (feature.title)}
      <div class="flex flex-col items-center gap-2 text-center md:flex-row md:gap-4 md:text-left mt-6">
        <img src={feature.image} alt={feature.title} class="dark:brightness-0 dark:invert-[1] mr-4 lg:mr-8"/> 
        <div>
          <h2 class="mt-10 scroll-m-20 pb-2 text-3xl font-semibold tracking-tight transition-colors first:mt-0">
            {feature.title}
          </h2>
          <p>{feature.description}</p>
        </div>
      </div>
    {/each}
  </div>

  <div class="md-border" style="background-image:url(/play.png);background-repeat:no-repeat;background-size:cover" />
</section>