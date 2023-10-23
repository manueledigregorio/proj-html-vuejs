
<script>
import FooterList from "./FooterList.vue";
import Form from "./partials/Form.vue";
import CarouselFooter from "./CarouselFooter.vue";
import Copyright from "./Copyright.vue"
export default {
  name:'Footer',

  components:{
    Form,
    CarouselFooter,
    FooterList,
    Copyright
  }
}
</script>

<template>

      <Form />
      <CarouselFooter />
      <FooterList />
      <Copyright />
  
</template>

<style lang="scss" scoped>

</style>