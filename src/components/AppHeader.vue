<template>
  <div class="ms-container">
    <div class="row py-4">
      <div class="col col-5">
        <div class="ms-img-container">
          <img src="../assets/img/logo-restaurant-2x-300x58.png" alt="logo" />
        </div>
      </div>
      <div class="col col-7">
        <ul>
          <li
            v-for="(item, index) in menuItems"
            :key="index"
            :class="{ isActive: item.active }"
          >
            <span v-if="item.isIcon">
              <font-awesome-icon :icon="`fa-solid ${item.name}`"
            /></span>
            <span v-else>
              {{ item.name }}
            </span>
            <span class="new" :class="{ isVisible: item.new }">New</span>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "AppHeader",
  props: {
    menuItems: Array,
  },
};
</script>

<style lang="scss" scoped>
.ms-container {
  width: 90%;
  margin: 0 auto;
}
.ms-img-container {
  width: 300px;
}

ul {
  display: flex;
  justify-content: space-around;
  align-items: center;
  width: 100%;
  height: 100%;

  li {
    color: #bcbcbc;
    font-size: 0.8rem;
    font-weight: 700;
    &.isActive {
      color: white;
    }

    .new {
      display: none;
      padding: 0.1rem 0.3rem;
      font-size: 0.5rem;
      border: 1px solid silver;
      line-height: 0.7rem;
      color: silver;
      vertical-align: middle;

      &.isVisible {
        display: inline-block;
      }
    }
  }
}
</style>
