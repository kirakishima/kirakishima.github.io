<script lang="ts">
  import { fly } from "svelte/transition";
  import { onMount } from "svelte";

  export let logoIndex: number;
  export let direction: string;

  let visible = false;

  const baseOffset = 25;
  let offsetX = 0;
  let offsetY = 0;

  function shiftElement() {
    if (direction === "top") {
      offsetY = baseOffset;
    } else if (direction === "bottom") {
      offsetY = -baseOffset;
    } else if (direction === "left") {
      offsetX = -baseOffset;
    } else if (direction === "right") {
      offsetX = baseOffset;
    }
  }

  onMount(async () => {
    shiftElement();
    visible = true;
  });
</script>

{#if visible}
  <div
    class="fixed h-1/5 md:h-2/5 lg:h-4/5 w-full flex justify-center select-none"
    transition:fly={{
      x: offsetX,
      y: offsetY,
      duration: (logoIndex + 2) * 200,
      delay: (logoIndex + 1) * 200,
    }}
  >
    <img
      draggable="false"
      class="absolute inline-block w-4/5"
      src={`/images/logo/${logoIndex.toString()}.svg`}
      alt="logo"
    />
  </div>{/if}
