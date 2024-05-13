<script lang="ts">
  import { t } from "$lib/translate.svelte";
</script>

<section class="h-screen">
  <h1
    class="mx-auto w-5/6 mt-10 text-4xl sm:text-5xl xl:text-7xl font-bold flex flex-col"
  >
    {$t("design.title")}
  </h1>
  <h2 class="text-4xl font-bold flex justify-evenly mt-64">
    {$t("design.strict")}
    {$t("design.delimiter")}
    {$t("design.catchy")}
  </h2>
</section>
