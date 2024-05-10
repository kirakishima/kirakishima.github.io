<script lang="ts">
  import MainLogo from "../images/mainLogo.svelte";
  import { onMount } from "svelte";
  interface Logo {
    index: number;
    direction: "top" | "bottom" | "left" | "right";
    delay: number;
  }
  const logos: Array<Logo> = [
    { index: 0, direction: "bottom", delay: 100 },
    { index: 1, direction: "bottom", delay: 100 },
    { index: 2, direction: "left", delay: 200 },
    { index: 3, direction: "right", delay: 200 },
    { index: 4, direction: "left", delay: 400 },
    { index: 5, direction: "right", delay: 600 },
    { index: 6, direction: "right", delay: 600 },
  ];
  let isLogoVisible: boolean = false;
  onMount(() => {
    setTimeout(() => {
      isLogoVisible = true;
    }, 100);
  });
</script>

<section class="mx-auto bg-gray-400 dark:bg-gray-800 h-screen">
  {#if isLogoVisible}
    {#each logos as logo}
      <MainLogo
        logoIndex={logo.index}
        delay={logo.delay}
        direction={logo.direction}
      />
    {/each}
  {/if}
</section>
