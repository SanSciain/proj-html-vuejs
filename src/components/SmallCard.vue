<template>
  <div class="card d-flex justify-content-center">
    <div class="ms-img-container">
      <img
        :src="require(`../assets/img/${cardContent.image}.png`)"
        class="card-img-top"
        alt=""
      />
    </div>
    <div class="card-body d-flex flex-column align-items-center">
      <h5 class="card-title">{{ cardContent.title }}</h5>
      <span class="line"></span>
      <p class="card-text">
        {{ cardContent.text }}
      </p>
      <a href="" class="btn ms-btn">{{ cardContent.btnText }}</a>
    </div>
  </div>
</template>

<script>
export default {
  name: "SmallCard",
  props: {
    cardContent: Object,
  },
};
</script>

<style lang="scss" scoped>
.card {
  border: none;
  width: calc(100% / 3.5);

  .ms-img-container {
    width: 20%;
    margin: 0 auto;
  }

  .card-title {
    font-weight: bold;
    text-transform: uppercase;
    text-align: center;
    font-family: "Oswald", sans-serif;
  }

  .line {
    border-bottom: 1px solid silver;
    display: inline-block;
    width: 50px;
    margin: 1rem 0;
  }

  .card-text {
    text-align: center;
  }

  .ms-btn {
    color: #434243;
    border-color: #434243;
  }
}
</style>
