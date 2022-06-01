<template>
  <div id="app">
    <AppHeader :menuItems="headerMenu" />
    <div class="ms-labels-wrapper">
      <div
        class="demos d-flex ms-label flex-column mb-2 text-center justify-content-center"
      >
        <font-awesome-icon icon="fa-solid fa-folder" class="main-label" />
        <span>Demos</span>
      </div>
      <div
        class="sale ms-label d-flex flex-column text-center justify-content-center"
      >
        <span class="main-label price">$39</span>
        <span>On Sale</span>
      </div>
    </div>
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
import { faFolder } from "@fortawesome/free-solid-svg-icons";
library.add(faFolder);
import { faChevronUp } from "@fortawesome/free-solid-svg-icons";
library.add(faChevronUp);
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
.ms-labels-wrapper {
  position: absolute;
  right: 2rem;
  top: 6rem;

  .ms-label {
    display: block;
    width: 60px;
    height: 60px;
    background-color: white;
    padding: 0.5rem;
    border-radius: 10px;
    font-size: 0.7rem;
    color: $ms-tundora;

    .main-label {
      font-size: 1.2rem;
    }

    .price {
      color: $ms-christi;
      font-weight: bold;
    }
  }
}
</style>
