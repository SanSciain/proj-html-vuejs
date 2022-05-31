<template>
  <div class="ms-container-small d-flex justify-content-around py-5">
    <SmallCard
      v-for="(item, index) in cardContent"
      :key="index"
      :cardContent="item"
    />
  </div>
</template>

<script>
import SmallCard from "./SmallCard.vue";
export default {
  name: "SmallCards",
  components: {
    SmallCard,
  },
  data() {
    return {
      cardContent: [
        {
          image: "sushi-1",
          title: "the best table in town",
          text: "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Reprehenderit temporibus vitae asperiores rem?",
          btnText: "explore the menu",
        },
        {
          image: "sushi-2",
          title: "perfect for groups",
          text: "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Reprehenderit temporibus vitae asperiores rem?",
          btnText: "make a reservetion",
        },
        {
          image: "sushi-3",
          title: "fresh produce everyday",
          text: "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Reprehenderit temporibus vitae asperiores rem?",
          btnText: "learn more about us",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped></style>
