<script>
export default {
  name: "BigCard",

  data() {
    return {};
  },
  props: {
    items: Object,
  },
};
</script>

<template>
  <div class="cards">
    <div class="hover-container">
      <div>
        <img class="img-hover" :src="items.img" alt="" />
      </div>

      <div class="hover-text d-flex flex-column">
        <div class="link">
          <a :href="items.href">
            <i
              class="d-flex justify-content-center align-items-center"
              :class="items.link"
            ></i>
          </a>
        </div>
        {{ items.title }}
      </div>
    </div>

    <div class="p-4">
      <h4 class="font">{{ items.title }}</h4>
      <p class="p-2">{{ items.subtitle }}</p>
      <hr />
      <p>{{ items.description }}</p>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "../../sass/partials/variabiles.scss" as *;
img {
  width: 100%;
}

p {
  color: $lightblack;
}

.hover-container {
  position: relative;
  overflow: hidden;

  .img-hover {
    width: 100%;
    height: 100%;
    transition: filter 0.5s;
    border-radius: 0;
  }
  &:hover .hover-text {
    opacity: 1;
  }
}

.hover-text {
  position: absolute;
  top: 0;
  left: 0;
  align-items: center;
  justify-content: center;
  display: flex;
  background: linear-gradient(
    transparent,
    rgba(255, 87, 31, 0.6),
    rgba(255, 87, 31, 1)
  );
  background-color: rgba(255, 87, 31, 0.5);
  color: #fff;
  padding: 10px;
  opacity: 0;
  transition: opacity 0.5s;
  width: 100%;
  height: 100%;

  i {
    width: 40px;
    height: 40px;
    background-color: $white;
    border-radius: 50%;
    color: rgba(1, 0, 0, 0.488);
  }
}
</style>
