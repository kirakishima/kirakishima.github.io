<script lang="ts">
  import MainLogo from "../images/mainLogo.svelte";
  import { onMount } from "svelte";
  interface Logo {
    direction: "top" | "bottom" | "left" | "right";
  }
  const logos: Array<Logo> = [
    { direction: "bottom" },
    { direction: "bottom" },
    { direction: "left" },
    { direction: "right" },
    { direction: "left" },
    { direction: "right" },
    { direction: "right" },
  ];
  let isLogoVisible: boolean = false;
  onMount(() => {
    setTimeout(() => {
      isLogoVisible = true;
    }, 100);
  });
</script>

<section
  class="mt-20 h-[40vh] sm:h-[60vh] md:h-[70vh] lg:h-[90vh] xl:h-screen flex justify-center"
>
  {#if isLogoVisible}
    {#each logos as logo, i}
      <MainLogo logoIndex={i} direction={logo.direction} />
    {/each}
  {/if}
</section>
