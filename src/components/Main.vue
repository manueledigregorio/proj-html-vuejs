<script>
import Hero from './partials/Hero.vue';
import Recipes from './partials/Recipes.vue';
import CulinaryColl from './partials/CulinaryColl.vue';
export default {
  name: 'Main',
  components:{
    Hero,
    Recipes,
    CulinaryColl,

  }
}
</script>

<template>
<main>
  <Hero />
  <Recipes/>
  <CulinaryColl />
</main>
    

  
</template>

<style lang="scss" scoped>

</style>