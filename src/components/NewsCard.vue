<template>
  <div class="card">
    <img
      :src="require(`../assets/img/${cardContent.img}`)"
      class="card-img-top"
      alt=""
    />
    <div class="card-body">
      <h5 class="card-title ms-title">{{ cardContent.title }}</h5>
      <p class="card-text">{{ cardContent.credits }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "NewsCard",
  props: {
    cardContent: Object,
  },
};
</script>

<style lang="scss" scoped>
@import "../style/variables.scss";
.card {
  border: none;
  border-radius: 0;

  img {
    min-height: 500px;
    object-fit: cover;
  }

  .card-body {
    text-align: center;

    .ms-title {
      font-size: 1.2rem;
    }

    .card-text {
      font-size: 0.6rem;
      color: $ms-tundora;
    }
  }
}
</style>
