<template>
  <div>
    <AppJumbo :jumboContent="jumbos[0]" />
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
  data() {
    return {
      jumbos: [
        {
          upperTitle: "the best table in town",
          title: "fine dining experience",
          text: "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ipsa, beatae. Lorem ipsum dolor sit amet.",
          btnText: "Explore the menu",
          label: true,
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped></style>
