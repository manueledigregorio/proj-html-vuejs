<script>
import BigCard from './BigCard.vue';
import {CardTwo} from '../../data/partials/bigCard';
export default {
name: 'FarmTable',
data() {
  return {
    CardTwo
  }
},
components:{
  BigCard,
}
}
</script>

<template>
  <div class="container ">

    <div class="row">
    <div class="col-8">
      <div >
        <h4>FARM TO TABLE</h4>
        <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Atque laborum qui ut maiores, tempore id nihil facilis minus quaerat doloribus!</p>
      </div>
      <div class="mycontainer">
        <BigCard 
        v-for="(items, index) in CardTwo"
        :key="index"
        :items="items" />
        <div class="px-4 d-flex justify-content-between ">
          <div>
            <a href="#">Read More</a>
            <i class="fa-solid fa-chevron-right"></i>
          </div>
          <div>
            <i class="fa-regular fa-comments"></i>
            <span>0</span>
          </div>
         
        </div>
      </div>
    </div>
    <div class="col-4"></div>
  </div>

  </div>
  
</template>

<style lang="scss" scoped>
@use "../../sass/partials/variabiles.scss" as *;
  .container{
    margin-top: 150px;
  }
   .mycontainer {
      width: 100%;
      background-color: $white;
      padding-bottom: 20px;
      margin-top: 80px;

      a{
        color: $lightblack;
      }
    }  
</style>