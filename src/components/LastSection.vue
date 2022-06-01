<template>
  <div class="wrapper position-relative">
    <img src="../assets/img/hero42x.jpg" alt="" />
    <div class="info-wrapper">
      <h3 class="ms-title">Braised<br />Abalone</h3>
      <div class="line py-2"></div>
      <p class="description">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Eum, doloremque
        fugiat. Saepe eius ipsum quis labore dignissimos
      </p>
      <span class="price">$52</span>
      <a class="btn ms-btn" href="" role="button">view the menu</a>
    </div>
  </div>
</template>

<script>
export default {
  name: "LastSection",
};
</script>

<style lang="scss" scoped>
.wrapper {
  height: 650px;
  color: white;

  img {
    height: 100%;
    object-fit: cover;
  }

  .info-wrapper {
    width: calc(100% / 4);
    padding: 4rem 3rem;
    position: absolute;
    background-color: black;
    top: 4rem;
    left: 10rem;

    .description {
      color: silver;
      padding: 2rem 0;
    }
    .price {
      color: silver;
      font-size: 0.8rem;
      font-weight: bold;
      position: absolute;
      top: 4rem;
      right: 2rem;
    }
  }
}
</style>
