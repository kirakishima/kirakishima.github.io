<script lang="ts">
  import ThemeSwitcher from "$lib/themes/themeSwitcher.svelte";
  import MainSection from "$lib/sections/mainSection.svelte";
  import DesignChoice from "$lib/sections/designChoice.svelte";
  import BonusesSection from "$lib/sections/bonusesSection.svelte";
  import WhyUs from "$lib/sections/whyUs.svelte";
</script>

<title>Home</title>
<ThemeSwitcher />

<div class="container mx-auto">
  <MainSection />
  <DesignChoice />
  <BonusesSection />
  <WhyUs />
</div>
