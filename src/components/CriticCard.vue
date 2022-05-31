<template>
  <div
    class="card"
    :style="{
      'background-image': 'url(' + cardContent.background + ')',
    }"
  >
    <div class="card-body d-flex flex-column">
      <div class="author">{{ cardContent.author }}</div>
      <h3 class="title my-4">{{ cardContent.newspaper }}</h3>
      <div class="stars">
        <font-awesome-icon
          icon="fa-solid fa-star"
          v-for="item in 5"
          :key="item"
          class="px-1"
        />
      </div>
      <span class="line"></span>
      <p class="my-3">{{ cardContent.text }}</p>
      <a class="btn ms-btn" href="" role="button">{{ cardContent.btnText }}</a>
    </div>
  </div>
</template>

<script>
import Vue from "vue";
import { FontAwesomeIcon } from "@fortawesome/vue-fontawesome";
import { library } from "@fortawesome/fontawesome-svg-core";
import { faStar } from "@fortawesome/free-solid-svg-icons";
library.add(faStar);
Vue.component("font-awesome-icon", FontAwesomeIcon);
export default {
  name: "CriticCard",
  props: {
    cardContent: Object,
  },
};
</script>

<style lang="scss" scoped>
.card {
  padding: 6rem;
  border-radius: 0;
  color: white;
  border: none;
  background-position: center;
  background-size: cover;

  .author {
    font-size: 0.7rem;
    text-transform: uppercase;
    color: silver;
    font-weight: 600;
  }

  .title {
    font-size: 2rem;
    text-transform: uppercase;
    font-family: "Oswald", sans-serif;
  }

  .stars {
    font-size: 0.7rem;
    margin: 2rem 0;
  }

  .ms-btn {
    width: fit-content;
  }
}
</style>
