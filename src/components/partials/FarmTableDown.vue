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
      class="col-6 card pt-2 ">
      <Card :cards="items"/> 
    </div>
    <button type="button" class="btn mt-4 bt btn-lg">LOAD MORE POSTS</button>
  </div>
  
</template>

<style lang="scss" scoped>
@use "../../sass/partials/variabiles.scss" as *;

.bt{
  background-color: $button;
  padding: 10px;
  border-radius: 0px;
}

.card{
  background-color: $background;
  border: 0;
}



</style>