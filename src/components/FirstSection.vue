<template>
  <div class="ms-container-small">
    <div class="row">
      <div class="col col-6 ms-col-text">
        <p>
          <span>Lorem ipsum dolor sit amet </span>
          Exercitationem obcaecati laudantium consequuntur inventore repudiandae
          ratione numquam laborum. Excepturi veritatis incidunt harum, soluta
          quisquam dignissimos. Error delectus reiciendis eaque totam incidunt
          ipsam. Fugit quam veritatis nulla necessitatibus amet quod harum
          quidem, ab illo voluptas eaque sapiente temporibus! Quasi, optio
          assumenda! Vel.
        </p>
        <h2 class="ms-title my-5">
          food is our common ground, a universal experience
        </h2>
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Porro quasi
          quidem doloribus vel expedita non nam tempore eligendi aspernatur
          dolore.
        </p>
        <div class="ms-signature-container">
          <img src="../assets/img/signature-200x172.jpg" alt="signature" />
        </div>
      </div>
      <div class="col col-6 ms-col-img position-relative">
        <div class="ms-img-container">
          <img src="../assets/img/info22x.jpg" alt="" />
        </div>
        <span class="description">california rolls - $22</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "FirstSection",
};
</script>

<style lang="scss" scoped>
.ms-container-small {
  padding: 7rem 0;
  .ms-col-text {
    padding-right: 3rem;

    span {
      font-weight: bold;
      text-transform: uppercase;
    }
    .ms-signature-container {
      width: 150px;
    }
  }

  .description {
    font-size: 0.7rem;
    color: white;
    text-transform: uppercase;
    font-weight: 700;
    display: inline-block;
    width: 100%;
    text-align: center;
    position: absolute;
    bottom: 2rem;
  }
}
</style>
