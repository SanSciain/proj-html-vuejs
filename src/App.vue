<template>
  <div id="app">
    <AppHeader :menuItems="headerMenu" class="fixed-top" />
    <AppMain />
    <AppFooter />
  </div>
</template>

<script>
import AppHeader from "./components/AppHeader.vue";
import AppMain from "./components/AppMain.vue";
import AppFooter from "./components/AppFooter.vue";

import Vue from "vue";
import { FontAwesomeIcon } from "@fortawesome/vue-fontawesome";
import { library } from "@fortawesome/fontawesome-svg-core";
import { faCartShopping } from "@fortawesome/free-solid-svg-icons";
library.add(faCartShopping);
Vue.component("font-awesome-icon", FontAwesomeIcon);

export default {
  name: "App",
  components: {
    AppHeader,
    AppMain,
    AppFooter,
  },
  data() {
    return {
      headerMenu: [
        {
          name: "Home",
          active: true,
          isIcon: false,
          new: false,
        },
        {
          name: "Culinary History",
          active: false,
          isIcon: false,
          new: false,
        },
        {
          name: "Our Team",
          active: false,
          isIcon: false,
          new: false,
        },
        {
          name: "Our Menu",
          active: false,
          isIcon: false,
          new: false,
        },
        {
          name: "Takeout",
          active: false,
          isIcon: false,
          new: true,
        },
        {
          name: "Bulletin",
          active: false,
          isIcon: false,
          new: false,
        },
        {
          name: "Reservations",
          active: false,
          isIcon: false,
          new: false,
        },
        {
          name: "fa-solid fa-cart-shopping",
          active: false,
          isIcon: true,
          new: false,
        },
      ],
    };
  },
};
</script>

<style lang="scss">
@import "./style/common.scss";
</style>
