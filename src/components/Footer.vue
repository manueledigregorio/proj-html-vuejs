
<script>
import FooterList from "./FooterList.vue";
import Form from "./partials/Form.vue";
import CarouselFooter from "./CarouselFooter.vue";
export default {
  name:'Footer',

  components:{
    Form,
    CarouselFooter,
    FooterList
  }
}
</script>

<template>

      <Form />
      <CarouselFooter />
      <FooterList />
  
</template>

<style lang="scss" scoped>

</style>