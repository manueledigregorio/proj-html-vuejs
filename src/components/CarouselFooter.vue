<script>
  import Carousel from '../data/partials/Carousel'
  // Import Swiper Vue.js components
  import { Swiper, SwiperSlide } from 'swiper/vue';

  // Import Swiper styles
  import 'swiper/css';
  // import required modules
  import { Autoplay } from 'swiper/modules';
  export default {
    components: {
      Swiper,
      SwiperSlide,
    },
    setup() {
      return {
        modules: [Autoplay],
        Carousel
      };
    },
  };
</script>

<template>
  <swiper
    :slidesPerView="4"
    :spaceBetween="0"
    :loop="true"
    :modules="modules"
    :autoplay="{delay: 2500,disableOnInteraction: false,}"
    class="mySwiper"
  >
    <swiper-slide v-for="(items, index) in Carousel" :key="index">
      <img :src="items.img" :alt="items.name">
    </swiper-slide>
  </swiper>
</template>

<style lang="scss" scoped>
img{
  width: 100%;
  object-fit: cover;
}
  
</style>
