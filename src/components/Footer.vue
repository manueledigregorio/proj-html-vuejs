
<script>
import FooterList from "./partials/FooterList.vue";
import Form from "./partials/Form.vue";
import CarouselFooter from "./partials/CarouselFooter.vue";
import Copyright from "./partials/Copyright.vue";
export default {
  name: "Footer",

  components: {
    Form,
    CarouselFooter,
    FooterList,
    Copyright,
  },
};
</script>

<template>
  <Form />
  <CarouselFooter />
  <FooterList />
  <Copyright />
</template>

<style lang="scss" scoped>
</style>