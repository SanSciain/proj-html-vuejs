<template>
  <div class="ms-wrapper">
    <div class="row">
      <div class="col col-5 ms-text-col">
        <span class="ms-line"></span>
        <div class="ms-text-wrapper">
          <span class="ms-upper-title">the best table in town</span>
          <h2 class="ms-title py-4">fine dining experience</h2>
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
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Vue from "vue";
import { FontAwesomeIcon } from "@fortawesome/vue-fontawesome";
import { library } from "@fortawesome/fontawesome-svg-core";
import { faFolder } from "@fortawesome/free-solid-svg-icons";
library.add(faFolder);
Vue.component("font-awesome-icon", FontAwesomeIcon);

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

      .ms-title {
        color: white;
      }
    }
  }

  .ms-img-col {
    // background-image: url("../assets/img/slider52x.jpg");
    padding: 0;
    position: relative;

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
        color: #434243;

        .main-label {
          font-size: 1.2rem;
        }

        .price {
          color: #69a10e;
          font-weight: bold;
        }
      }
    }
  }
}
</style>
