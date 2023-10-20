<script>
import Hero from './partials/Hero.vue';
import Recipes from './partials/Recipes.vue';
export default {
  name: 'Main',
  components:{
    Hero,
    Recipes,

  }
}
</script>

<template>
<main>
  <Hero />
  <Recipes/>
</main>
    

  
</template>

<style lang="scss" scoped>

</style>