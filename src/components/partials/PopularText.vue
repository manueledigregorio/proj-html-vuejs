<script>
import popular from "../../data/partials/popular";
export default {
  name: "PopularText",
  data() {
    return {
      popular,
    };
  },
};
</script>

<template>
  <div class="container-popular w-100 d-flex mb-5">
    <div
      class="d-flex p-3 justify-content-center align-items-center popular w-50"
    >
      <p class="font">Popular</p>
    </div>
    <div class="d-flex p-3 justify-content-center align-items-center w-50">
      <p class="font">Recent</p>
    </div>
  </div>
  <div class="mt-4">
    <div
      v-for="(items, index) in popular"
      :key="index"
      class="text mt-3 d-flex"
    >
      <div class="p-1">
        <img :src="items.image" alt="" />
      </div>
      <div>
        <p>
          {{ items.text }}
        </p>
        <p class="color">{{ items.data }}</p>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "../../sass/partials/variabiles.scss" as *;

.container-popular {
  border: 1px solid gainsboro;

  .popular {
    border-right: 1px solid gainsboro;
    text-align: center;
    background-color: $white;
  }
  p {
    font-size: 1.2rem;
  }
}
.text {
  img {
    width: 50px;
    height: 50px;
    border-radius: 50%;
    margin-right: 10px;
  }

  .color {
    color: $greey;
    font-size: 0.8rem;
  }
}
</style>