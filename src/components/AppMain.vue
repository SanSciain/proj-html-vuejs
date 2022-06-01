<template>
  <div>
    <AppJumbo :jumboContent="jumbos[0]" />
    <FirstSection />
    <SmallCards />
    <AppJumbo :jumboContent="jumbos[1]" />
    <CriticSection />
    <MidBanner />
    <NewsSection />
    <AppJumbo :jumboContent="jumbos[2]" />
  </div>
</template>

<script>
import Vue from "vue";
import { FontAwesomeIcon } from "@fortawesome/vue-fontawesome";
import { library } from "@fortawesome/fontawesome-svg-core";
import { faCar } from "@fortawesome/free-solid-svg-icons";
library.add(faCar);
Vue.component("font-awesome-icon", FontAwesomeIcon);

import AppJumbo from "./AppJumbo.vue";
import FirstSection from "./FirstSection.vue";
import SmallCards from "./SmallCards.vue";
import CriticSection from "./CriticSection.vue";
import MidBanner from "./MidBanner.vue";
import NewsSection from "./NewsSection.vue";
export default {
  name: "AppMain",
  components: {
    AppJumbo,
    FirstSection,
    SmallCards,
    CriticSection,
    MidBanner,
    NewsSection,
  },
  data() {
    return {
      jumbos: [
        {
          upperTitle: "the best table in town",
          title: "fine dining experience",
          text: "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ipsa, beatae. Lorem ipsum dolor sit amet.",
          btnText: "Explore the menu",
          img: "slider52x.jpg",
          reverse: false,
        },
        {
          upperTitle: "fine dining experience",
          title: "the best table in town",
          text: "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ipsa, beatae. Lorem ipsum dolor sit amet.",
          btnText: "Explore the menu",
          img: "slider32x.jpg",
          reverse: true,
        },
        {
          upperTitle: "enjoy your meal at home",
          title: "takeout now available",
          text: "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ipsa, beatae. Lorem ipsum dolor sit amet.",
          btnText: ["View takeout menu", "fa-solid fa-car"],
          img: "slider72x-scaled.jpg",
          reverse: true,
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped></style>
