<template>
  <div class="ms-container-small py-5">
    <div class="title-wrapper my-3">
      <h2 class="cursive-title">Latest news & promotions</h2>
      <span class="line"></span>
    </div>
    <div class="card-wrapper d-flex">
      <NewsCard
        v-for="(item, index) in cardContent"
        :key="index"
        :cardContent="item"
        class="mx-3"
      />
    </div>
  </div>
</template>

<script>
import NewsCard from "./NewsCard.vue";
export default {
  name: "NewsSection",
  components: { NewsCard },
  data() {
    return {
      cardContent: [
        {
          img: "blog92x.jpg",
          title: "the best coffee in town",
          credits: "By admin | January 7th, 2020 | Categories: News",
        },
        {
          img: "blog72x.jpg",
          title: "discover our new menu",
          credits: "By admin | January 7th, 2020 | Categories: News",
        },
        {
          img: "blog82x.jpg",
          title: "we now accept square",
          credits: "By admin | January 7th, 2020 | Categories: News",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import url("https://fonts.googleapis.com/css2?family=Cookie&display=swap");
.title-wrapper {
  text-align: center;

  .cursive-title {
    font-family: "Cookie", cursive;
    font-size: 3rem;
  }
}
</style>
