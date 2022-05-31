<template>
  <div class="ms-container-small py-5">
    <div class="title-wrapper my-3">
      <h2 class="cursive-title">What critics are saying about us</h2>
      <span class="line"></span>
    </div>
    <div class="row gx-0 my-4">
      <div class="col col-6">
        <div class="ms-img-container">
          <img src="../assets/img/blog72x.jpg" alt="" />
        </div>
      </div>
      <div class="col col-6">
        <CriticCard :cardContent="cardContent[0]" />
      </div>
    </div>
    <div class="cards-wrapper d-flex">
      <CriticCard
        class="m-2"
        v-for="index in 2"
        :key="index"
        :cardContent="cardContent[index]"
      />
    </div>
  </div>
</template>

<script>
import CriticCard from "./CriticCard.vue";
export default {
  name: "CriticSection",
  data() {
    return {
      cardContent: [
        {
          author: "meggy stewart",
          newspaper: "new york times",
          text: "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Dicta voluptatibus eveniet dolor ratione, voluptatum ad! Ipsa illo corrupti iste dignissimos, corporis",
          // background: "info12x.jpg",
          //sorry non avevo altre idee
          background:
            "data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wCEAAkGBw8NDw0PEBANDQ8PDQ0NDQ0NDQ8NDQ0NFREWFhURFRUYHSggGBolGxUVITEhJSk3LjouFx8zODMtNygtLisBCgoKBQUFDgUFDisZExkrKysrKysrKysrKysrKysrKysrKysrKysrKysrKysrKysrKysrKysrKysrKysrKysrK//AABEIAOEA4QMBIgACEQEDEQH/xAAXAAEBAQEAAAAAAAAAAAAAAAAAAQIH/8QAGRABAQEBAQEAAAAAAAAAAAAAABEBQTEC/8QAFAEBAAAAAAAAAAAAAAAAAAAAAP/EABQRAQAAAAAAAAAAAAAAAAAAAAD/2gAMAwEAAhEDEQA/AOIkWGYAiw3ANQWAJCAKRIoJBUgARYCLuG4gApASEWGYAiw3ANQWAJCAKRIoIqKARIQAVICwiLAEAFhCJAUiRYBEikBCEIAoQAiQgAqQFhEWAIALCESAQIALEICpCEBUipAFRQIkWAJFAEFiQAFgJBUgCxCAqQhAVIqQBUUCJFgAABEhFAQICxILAEgQAhFBIokBRIQBYgCooBEhFAQICxILAEgQAIsACKDMIsAQWAARIBAgAqAEVIoBuJFgIsEgLEVAIRYAgsAAiQCBABUAIrMAaSEABQCJDACAQAigJFAEgsSAbiwQCBFgCQABQCJDACAQAigEABIpEAhAgLASApEIAqKCBACEWAJAgBFiQgEUiAQgQFgJAUiEABQBACLEhAAgBFiRYCKiwEhFSApEhAAiwEhFSAAQCLEhAAgBFiRYCKiwEhFSAKgCxIEAIQBYEQCKgCpioCxIALEzFSALEIAsIARIEAIQBYEQCKgCpioBFRQQiwzAEWG4BqCwBIQBSJFBIKkBUIsBFhuIAKQEIsMwBFhuAagsASEAUiRQRUUAiQgAqQFhEWAIALCESApEiwCJFICEIQBQgBEhABUgLCIsAQAWEIkAgQAWIQFSEICpFSAKigRIsASKAILEgALASCpAFiEBUhCAqRUgCooESLAAACJCKAgQFiQWAJAgBCKCRRICiQgCxAFRQCJCKAgQFiQWAJAgARYAEUGYRYAgoAGYkAgQAVACKkUA3EiwEWCQFiKgEIsAQUADMSAQIAKgBFZgDWAAmrwAMRQEMUBDVATTPAATFAPoAFNAExQBNXgAYigIYoCGqAAA/9k=",
          bgflag: false,
          btnText: "read full article",
        },
        {
          author: "mary maxey",
          newspaper: "the guardian",
          text: "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Dicta voluptatibus eveniet dolor ratione, voluptatum ad! Ipsa illo corrupti iste dignissimos, corporis",
          background: require("../assets/img/info52x.jpg"),
          bgflag: true,
          btnText: "read full article",
        },
        {
          author: "partick monore",
          newspaper: "globe and mail",
          text: "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Dicta voluptatibus eveniet dolor ratione, voluptatum ad! Ipsa illo corrupti iste dignissimos, corporis",
          background: require("../assets/img/info12x.jpg"),
          bgflag: true,
          btnText: "read full article",
        },
      ],
    };
  },
  components: { CriticCard },
};
</script>

<style lang="scss" scoped>
@import url("https://fonts.googleapis.com/css2?family=Cookie&display=swap");
.title-wrapper {
  text-align: center;

  .cursive-title {
    font-family: "Cookie", cursive;
    font-size: 3rem;
  }
}

.ms-img-container {
  height: 100%;
  width: 100%;
}

img {
  height: 100%;
  width: 100%;
  object-fit: cover;
}
</style>
