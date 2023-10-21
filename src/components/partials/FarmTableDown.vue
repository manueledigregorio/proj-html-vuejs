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
        <Card 
         
          :cards="items"
        />
      </div>
    <div class="col-4">

      <div class="search d-flex align-items-center justify-content-center">
          <div class="header-center px-3 d-flex align-items-center ">
            <div class="t-search">
              <i class="fa-solid fa-magnifying-glass"></i>
            </div>
            <div class="form-search">
              <input 
                v-model="search"
                class="form-control custom-input me-2" type="search"
                placeholder="Seach" aria-label="Search" 
              />
            </div>
          </div>
        </div>

    </div>


  </div>
  
</template>

<style lang="scss" scoped>

.search {
  background-color: whitesmoke;
  width: 100%;
  height: 50px;

  .header-center {
    background-color: white;
    width: 95%;

     i{
      color: #B1B1B1;
    }
  }
  .t-search{
    width: 15%;
    text-align: center;
  }

  .custom-input {
    background-color: white;
    box-shadow: none;
    border: none;
  }
}


</style>