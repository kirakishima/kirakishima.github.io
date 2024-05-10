<script>
  import { fly } from "svelte/transition";
  import { onMount } from "svelte";

  let visible = false;
  export let delay = 0;
  export let logoIndex = 0;
  export let direction = "top";
  let offsetX = 0;
  let offsetY = 0;

  function shiftElement() {
    if (direction === "top") {
      offsetY = 50;
    } else if (direction === "bottom") {
      offsetY = -50;
    } else if (direction === "left") {
      offsetX = -50;
    } else if (direction === "right") {
      offsetX = 50;
    }
  }

  onMount(async () => {
    shiftElement();
    visible = true;
  });
</script>

{#if visible}
  <div
    transition:fly={{
      x: offsetX,
      y: offsetY,
      duration: (logoIndex + 2) * 200,
      delay: delay,
    }}
  >
    <img
      class="absolute top-0"
      src={`/images/logo/${logoIndex.toString()}.svg`}
      alt="logo"
    />
  </div>{/if}
