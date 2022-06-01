<template>
  <footer class="text-center">
    <div class="upper-footer d-flex justify-content-center py-5">
      <div class="wrapper">
        <div class="ms-img-container">
          <img src="../assets/img/logo-restaurant-2x.png" alt="logo" />
        </div>
        <p class="py-5">
          Lorem ipsum dolor, sit amet consectetur adipisicing elit. Repudiandae,
          quos! Lorem ipsum dolor sit amet.
        </p>
        <div class="icons-wrapper">
          <font-awesome-icon
            v-for="(item, index) in icons"
            :key="index"
            :icon="`fa-brands ${item}`"
          />
        </div>
      </div>
    </div>
    <div class="bottom-footer text-center">
      <p>
        Copyright 2012 - 2019 Avada | All Rights Reserved | Powered by
        <span>WordPress</span> | <span>ThemeFusion</span>
      </p>
      <div class="arrow">
        <font-awesome-icon icon="fa-solid fa-chevron-up" />
      </div>
    </div>
  </footer>
</template>

<script>
import Vue from "vue";
import { FontAwesomeIcon } from "@fortawesome/vue-fontawesome";
import { library } from "@fortawesome/fontawesome-svg-core";
import { faChevronUp } from "@fortawesome/free-solid-svg-icons";
library.add(faChevronUp);
Vue.component("font-awesome-icon", FontAwesomeIcon);
export default {
  name: "AppFooter",
  props: {
    icons: Array,
  },
};
</script>

<style lang="scss" scoped>
@import "../style/variables.scss";
.upper-footer {
  background-image: url("../assets/img/footer2x.jpg");
  background-position: center;
  background-size: cover;

  .wrapper {
    width: calc(100% / 3);
    padding: 8rem 0;

    .ms-img-container {
      width: 60%;
      margin: 0 auto;
    }

    p {
      color: silver;
    }
  }
}

.bottom-footer {
  background-color: black;
  padding: 1rem;
  position: relative;

  p {
    font-size: 0.6rem;
    margin: 0;
    color: $ms-silver;

    span {
      font-weight: bold;
    }
  }

  .arrow {
    position: absolute;
    padding: 0.3rem;
    bottom: 0;
    right: 5rem;
    width: 30px;
    height: 20px;
    background: $ms-tundora;
    color: $ms-silver;
    line-height: 0;
    font-size: 0.6rem;
  }
}
</style>
