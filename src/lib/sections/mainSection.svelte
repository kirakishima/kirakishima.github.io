<script lang="ts">
  import MainLogo from "../images/mainLogo.svelte";
  import { onMount } from "svelte";
  interface Logo {
    index: number;
    direction: "top" | "bottom" | "left" | "right";
  }
  const logos: Array<Logo> = [
    { index: 0, direction: "bottom" },
    { index: 1, direction: "bottom" },
    { index: 2, direction: "left" },
    { index: 3, direction: "right" },
    { index: 4, direction: "left" },
    { index: 5, direction: "right" },
    { index: 6, direction: "right" },
  ];
  let isLogoVisible: boolean = false;
  onMount(() => {
    setTimeout(() => {
      isLogoVisible = true;
    }, 100);
  });
</script>

<section class="mt-12 flex justify-center">
  {#if isLogoVisible}
    {#each logos as logo}
      <MainLogo logoIndex={logo.index} direction={logo.direction} />
    {/each}
  {/if}
</section>
