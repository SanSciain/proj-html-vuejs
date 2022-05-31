<template>
  <div class="ms-wrapper">
    <div class="row g-0">
      <div class="col col-5 ms-text-col">
        <span class="ms-line"></span>
        <div class="ms-text-wrapper">
          <span class="ms-upper-title">{{ jumboContent.upperTitle }}</span>
          <h2 class="ms-title py-4">{{ jumboContent.title }}</h2>
          <p class="py-4">
            {{ jumboContent.text }}
          </p>
          <a class="btn ms-btn" href="" role="button">{{
            jumboContent.btnText
          }}</a>
        </div>
      </div>
      <div class="col col-7 ms-img-col">
        <div class="ms-img-container">
          <img src="../assets/img/slider52x.jpg" alt="" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "AppJumbo",
  props: {
    jumboContent: Object,
  },
};
</script>

<style lang="scss" scoped>
.ms-wrapper {
  color: silver;

  .ms-text-col {
    background-color: black;
    padding: 15rem 5rem 0rem 5.5rem;
    text-transform: uppercase;
    position: relative;

    .ms-line {
      border-bottom: 1px solid silver;
      display: inline-block;
      width: 40px;
      height: 0;
      position: absolute;
      top: 15.7rem;
    }

    .ms-text-wrapper {
      padding-left: 6rem;
      width: 90%;
      .ms-upper-title {
        font-size: 0.7rem;
      }

      .ms-title {
        color: white;
      }
    }
  }
}
</style>
