<template>
  <div>
    <AppJumbo />
    <FirstSection />
    <SmallCards />
  </div>
</template>

<script>
import AppJumbo from "./AppJumbo.vue";
import FirstSection from "./FirstSection.vue";
import SmallCards from "./SmallCards.vue";
export default {
  name: "AppMain",
  components: {
    AppJumbo,
    FirstSection,
    SmallCards,
  },
};
</script>

<style lang="scss" scoped></style>
