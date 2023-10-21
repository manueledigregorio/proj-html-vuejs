<script>
import Hero from './partials/Hero.vue';
import Recipes from './partials/Recipes.vue';
import CulinaryColl from './partials/CulinaryColl.vue';
import FarmTable from './partials/FarmTable.vue';

export default {
  name: 'Main',
  components:{
    Hero,
    Recipes,
    CulinaryColl,
    FarmTable,

  }
}
</script>

<template>
<main>
  <Hero />
  <Recipes/>
  <CulinaryColl />
  <FarmTable />
</main>
    

  
</template>

<style lang="scss" scoped>

</style>