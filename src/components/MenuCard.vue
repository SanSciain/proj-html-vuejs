<template>
  <div
    class="menu-card"
    :style="{
      'background-image': 'url(' + menuContent.bg + ')',
      'background-color': menuContent.bg,
    }"
  >
    <div class="ms-card-body">
      <h4 class="ms-title pb-5" :class="{ invert: menuContent.isBgImg }">
        {{ menuContent.title }}
      </h4>
      <div class="menu-item-wrapper">
        <MenuItem
          v-for="(item, index) in menuContent.menuList"
          :key="index"
          :menuItem="item"
          :reverse="menuContent.isBgImg"
        />
      </div>
    </div>
    <div :class="{ overlay: menuContent.isBgImg }"></div>
  </div>
</template>

<script>
import MenuItem from "./MenuItem.vue";
export default {
  name: "MenuCard",
  props: {
    menuContent: Object,
  },
  components: { MenuItem },
};
</script>

<style lang="scss" scoped>
@import "../style/overlay.scss";
.menu-card {
  background-position: center;
  background-size: cover;
  position: relative;
  z-index: -2;

  .ms-card-body {
    padding: 7rem 5rem;

    .ms-title {
      font-size: 2rem;

      &.invert {
        color: white;
      }
    }
  }
}
</style>
