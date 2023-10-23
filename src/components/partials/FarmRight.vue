
<script>
export default {
  name: "FarmRight",
};
</script>

<template>
  <div class="image-bg">
    <div class="cont-text text-center">
      <h5>VIEW OUR LATEST RECIPES</h5>
    </div>
  </div>

  <div class="container-down pt-5 position-relative">
    <img class="w-100" src="/singapore-featured-image-400x263.jpg" alt="" />
    <div class="text position-absolute">
      <p>City Guide: Singapore</p>
    </div>
    <div>
      <a class="d-flex justify-content-center pt-2" href="#">
        <i class="fa-solid fa-earth-americas"></i>
        <p>VIEW ALL GUIDES CITY</p>
      </a>
    </div>
  </div>

  <div class="line mt-5"></div>
</template>


<style lang="scss" scoped>
@use "../../sass/partials/variabiles.scss" as *;

.image-bg {
  background-image: url(public/ad-bg.jpg);
  background-size: cover;
  background-position: center;
  height: 410px;
  width: 100%; /* Imposta la larghezza al 100% */
  margin-top: 80px;

  .cont-text {
    width: 100%;
    height: 100%;
    padding: 160px 120px;

    h5 {
      line-height: 1.9rem;
    }
  }
}

.container-down {
  .text {
    top: 170px;
    background-color: rgba(0, 0, 0, 0.8);

    p {
      font-size: 1.3rem;
      color: $white;
      margin: 8px 15px;
    }
  }

  a {
    background-color: $orange;
    color: $white;
  }

  i {
    margin: 5px 10px;
  }
}
.line {
  border: 1px solid gainsboro;
}
</style>