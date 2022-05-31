<template>
  <div class="ms-wrapper">
    <div class="row">
      <div class="col col-5 ms-text-col">
        <span class="ms-line"></span>
        <div class="ms-text-wrapper">
          <span class="ms-upper-title">the best table in town</span>
          <h2 class="py-4">fine dining experience</h2>
          <p class="py-4">
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ipsa,
            beatae. Lorem ipsum dolor sit amet.
          </p>
          <a class="btn ms-btn" href="" role="button">Explore the menu</a>
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

      h2 {
        color: white;
        font-weight: bolder;
        font-size: 3rem;
      }

      .ms-btn {
        color: white;
        border: 1px solid white;
        border-radius: 0;
        font-size: 0.7rem;
        padding: 0.5rem 1.5rem;
        font-weight: 600;
      }
    }
  }

  .ms-img-col {
    // background-image: url("../assets/img/slider52x.jpg");
    padding: 0;
  }
}
</style>
