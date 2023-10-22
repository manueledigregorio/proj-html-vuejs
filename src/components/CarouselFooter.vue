<script>
  // Import Swiper Vue.js components
  import { Swiper, SwiperSlide } from 'swiper/vue';

  // Import Swiper styles
  import 'swiper/css';

  import 'swiper/css/pagination';

  // import required modules
  import { Pagination } from 'swiper/modules';
  export default {
    components: {
      Swiper,
      SwiperSlide,
    },
    setup() {
      return {
        modules: [Pagination],
      };
    },
  };
</script>

<template>
  <swiper
    :slidesPerView="4"
    :spaceBetween="50"
    :pagination="{
      clickable: true,
    }"
    :modules="modules"
    class="mySwiper"
  >
    <swiper-slide><img src="public/Yogurt-Nan-400x263.jpg" alt=""></swiper-slide>
    <swiper-slide><img src="public/r-rachel-park-366508-unsplash-min-400x263.jpg" alt=""></swiper-slide>
    <swiper-slide><img src="public/fi-korean-food-400x263.jpg" alt=""></swiper-slide>
    <swiper-slide><img src="public/Yogurt-Nan-400x263.jpg" alt=""></swiper-slide>
    <swiper-slide><img src=" public/Mixed-fruits-400x263.jpg" alt=""></swiper-slide>
    <swiper-slide><img src="public/r-michelle-tsang-500721-unsplash-min-400x263.jpg" alt=""></swiper-slide>
    <swiper-slide><img src=" public/Mixed-fruits-400x263.jpg" alt=""></swiper-slide>
    <swiper-slide><img src="public/fi-toasts-400x263.jpg" alt=""></swiper-slide>
    <swiper-slide><img src="public/fi-roundup-400x263.jpg" alt=""></swiper-slide>
  </swiper>
</template>

<style lang="scss" scoped>

</style>
