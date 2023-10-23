<script>
export default {
  name: "CardTweet",
};
</script>

<template>
  <div class="container-tweet">
    <div class="d-flex align-items-center justify-content-between">
      <div class="text d-flex align-items-center">
        <h4>Tweets</h4>
        <span class="px-1"> by </span>
        <a href="#"> @Theme_Fusion</a>
      </div>
      <div>
        <a href="#">
          <i class="color fa-solid fa-circle-exclamation"></i>
        </a>
      </div>
    </div>

    <div>
      <div class="mt-3 d-flex justify-content-between">
        <div class="top-tweet d-flex">
          <img src="/logotweet.png" alt="" />
          <div>
            <p>
              <b>Theme Fusion</b>
            </p>
            <p class="color">@Theme_Fusion</p>
          </div>
        </div>

        <i class="color fa-brands fa-twitter"></i>
      </div>

      <div class="ps-5 bottom">
        <p>
          Lorem ipsum dolor, sit amet consectetur adipisicing elit. Saepe aut
          iusto culpa possimus laudantium, quasi nesciunt perspiciatis suscipit?
          Repudiandae, iste. amet consectetur adipisicing elit. Saepe aut iusto
          culpa possimus laudantium,
        </p>
        <img class="mb-2" src="/Imgtweet.jpeg" alt="" />

        <div class="d-flex justify-content-between">
          <div>
            <i class="color px-3 fa-regular fa-heart"></i>
            <i class="color fa-solid fa-arrow-right-from-bracket"></i>
          </div>
          <span>21h</span>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "../../sass/partials/variabiles.scss" as *;
.container-tweet {
  background-color: $white;
  margin-top: 40px;
  border-radius: 5px;
  padding: 25px;

  .text {
    span {
      font-size: 0.5;
    }
  }

  .color {
    color: gainsboro;
    &:hover {
      color: $greey;
    }
  }

  .top-tweet {
    img {
      width: 30px;
      height: 30px;
      margin-right: 10px;
    }
  }

  .bottom {
    img {
      width: 100%;
      padding-top: 20px;
    }
  }
}
</style>