<template>
  <div>
    <AppJumbo />
    <FirstSection />
  </div>
</template>

<script>
import AppJumbo from "./AppJumbo.vue";
import FirstSection from "./FirstSection.vue";
export default {
  name: "AppMain",
  components: {
    AppJumbo,
    FirstSection,
  },
};
</script>

<style lang="scss" scoped></style>
