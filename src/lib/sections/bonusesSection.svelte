<script lang="ts">
  import { t } from "$lib/translate.svelte";
  let shared = {
    image: "rounded-xl",
  };
  let mobile = {
    section: "h-100 xl:hidden flex flex-col justify-center gap-y-10",
    image: "max-w-full mx-10 lg:mx-48",
    text: "text-5xl font-bold",
  };
  let pc = {
    section: "h-screen hidden xl:block",
    titleDiv: "text-6xl font-bold grid grid-cols-3 gap-10 text-center",
    text: "col-span-1",
    imageDiv: "flex flex-row justify-between mt-20",
    image: "w-1/3",
  };
</script>

<section class={pc.section}>
  <div class={pc.titleDiv}>
    <h2 class={pc.text}>{$t("bonuses.adapt.title")}</h2>
    <span class={pc.text}>{$t("bonuses.delimiter")}</span>
    <h2 class={pc.text}>{$t("bonuses.create.title")}</h2>
  </div>
  <div class={pc.imageDiv}>
    <img
      class={`${shared.image} ${pc.image}`}
      src={$t("bonuses.adapt.image.src")}
      alt={$t("bonuses.adapt.image.alt")}
    />
    <img
      class={`${shared.image} ${pc.image}`}
      src={$t("bonuses.create.image.src")}
      alt={$t("bonuses.create.image.alt")}
    />
  </div>
</section>

<section class={mobile.section}>
  <h2 class={mobile.text}>{$t("bonuses.adapt.title")}</h2>
  <img
    class={`${shared.image} ${mobile.image}`}
    src={$t("bonuses.adapt.image.src")}
    alt={$t("bonuses.adapt.image.alt")}
  />
  <span class={mobile.text}>{$t("bonuses.delimiter")}</span>
  <h2 class={mobile.text}>{$t("bonuses.create.title")}</h2>
  <img
    class={`${shared.image} ${mobile.image}`}
    src={$t("bonuses.create.image.src")}
    alt={$t("bonuses.create.image.alt")}
  />
</section>
