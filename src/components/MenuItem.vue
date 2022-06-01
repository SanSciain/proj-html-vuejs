<template>
  <div class="menu-item position-relative">
    <h5 class="ms-title" :class="{ invert: reverse }">
      {{ menuItem.name }}
    </h5>
    <p class="description" :class="{ invert: reverse }">
      {{ menuItem.description }}
    </p>
    <span class="price" :class="{ invert: reverse }">{{ menuItem.price }}</span>
  </div>
</template>

<script>
export default {
  name: "MenuItem",
  props: {
    menuItem: Object,
    reverse: Boolean,
  },
};
</script>

<style lang="scss" scoped>
.ms-title {
  font-size: 1.2rem;
  &.invert {
    color: white;
  }
}

.description {
  &.invert {
    color: silver;
  }
}

.price {
  font-size: 0.8rem;
  font-weight: bold;
  position: absolute;
  top: 0.5rem;
  right: 2rem;

  &.invert {
    color: silver;
  }
}
</style>
