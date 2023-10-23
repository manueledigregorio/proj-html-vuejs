
<script>
import icon from "../../data/partials/icon";
export default {
  name: "FollowUs",

  data() {
    return {
      icon,
    };
  },
};
</script>

<template>
  <div class="container-follow font">
    <h5>Follow Us</h5>

    <ul class="mt-4 p-0 d-flex">
      <li
        class="d-flex justify-content-center align-items-center"
        v-for="(items, index) in icon"
        :key="index"
      >
        <a :href="items.href">
          <i :class="items.brand"></i>
        </a>
      </li>
    </ul>
  </div>
</template>


<style lang="scss" scoped>
@use "../../sass/partials/variabiles.scss" as *;
.container-follow {
  h5 {
    color: $orange;
    padding-top: 50px;
  }

  li {
    background-color: #edede8;
    aspect-ratio: 1/1;
    width: 35px;
    border-radius: 5px;
    border: 1px solid gainsboro;
    margin-left: 10px;
  }

  i {
    color: $lightblack;
  }
}
</style>