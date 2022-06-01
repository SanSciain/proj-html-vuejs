<template>
  <div class="container">
    <div class="row g-0">
      <div class="col" v-for="(item, index) in menuContent" :key="index">
        <MenuCard :menuContent="item" :class="{ upper: item.isActive }" />
      </div>
    </div>
  </div>
</template>

<script>
import MenuCard from "./MenuCard.vue";
export default {
  name: "MenuSection",
  components: { MenuCard },
  data() {
    return {
      menuContent: [
        {
          title: "Hors d'oeuvres",
          isActive: false,
          menuList: [
            {
              name: "ahi salmon nigiri",
              price: "$48",
              description:
                "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Repellat, sint?",
            },
            {
              name: "ahi salmon nigiri",
              price: "$48",
              description:
                "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Repellat, sint?",
            },
            {
              name: "ahi salmon nigiri",
              price: "$48",
              description:
                "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Repellat, sint?",
            },
            {
              name: "ahi salmon nigiri",
              price: "$48",
              description:
                "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Repellat, sint?",
            },
          ],
          isBgImg: false,
          bg: "#e8e8e8",
        },
        {
          title: "main course",
          isActive: true,
          menuList: [
            {
              name: "ahi salmon nigiri",
              price: "$48",
              description:
                "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Repellat, sint?",
            },
            {
              name: "ahi salmon nigiri",
              price: "$48",
              description:
                "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Repellat, sint?",
            },
            {
              name: "ahi salmon nigiri",
              price: "$48",
              description:
                "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Repellat, sint?",
            },
            {
              name: "ahi salmon nigiri",
              price: "$48",
              description:
                "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Repellat, sint?",
            },
          ],
          isBgImg: true,
          bg: require("../assets/img/misc22x.jpg"),
        },
        {
          title: "dessert",
          isActive: false,
          menuList: [
            {
              name: "ahi salmon nigiri",
              price: "$48",
              description:
                "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Repellat, sint?",
            },
            {
              name: "ahi salmon nigiri",
              price: "$48",
              description:
                "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Repellat, sint?",
            },
            {
              name: "ahi salmon nigiri",
              price: "$48",
              description:
                "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Repellat, sint?",
            },
            {
              name: "ahi salmon nigiri",
              price: "$48",
              description:
                "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Repellat, sint?",
            },
          ],
          isBgImg: false,
          bg: "#e8e8e8",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.container {
  padding: 7rem 0;

  .upper {
    position: relative;
    top: -2rem;
  }
}
</style>
