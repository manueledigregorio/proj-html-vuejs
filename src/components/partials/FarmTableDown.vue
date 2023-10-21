<script>
import Card from './Card.vue';
import cardFarmDown from '../../data/partials/cardFarmDown'
export default {
  name:"FarmTableDown",
  data() {
    return {
      cardFarmDown
    }
  },

  components:{
    Card
  }
}
</script>

<template>
  <div class="row">
    <div 
      v-for="(items, index) in cardFarmDown" 
      :key="index" 
      class="col-6 pt-2 ">
      <Card :cards="items"/>

      
        
    </div>
  </div>
  
</template>

<style lang="scss" scoped>




</style>