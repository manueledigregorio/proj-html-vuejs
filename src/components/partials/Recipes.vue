<script>
import imgRecepies from '../../data/partials/imgRecepies';
import BigCard from './BigCard.vue';
import { CardOne } from '../../data/partials/bigCard';
export default {
  name: "Recipes",

  data() {
    return {
      imgRecepies,
      CardOne
    }
  },
  components:{
    BigCard,
    
  }
};
</script>

<template>
  <div class="container">
    <div class="d-flex justify-content-center">
      <div class="text">
        <h4>POPULAR RECIPES</h4>
        <p>
          Aliquam erat volutpat.Ut quis Lorem, ipsum reiciendis iusto,
          blanditiis hic deserunt accusantium ullam mollitia delectus.
        </p>
      </div>
    </div>
    <div class=" ">
      <div class="d-flex">
        <div class="col-6 me-2 ">
          <div class="mycontainer ">

            <BigCard 
            v-for="(items, index) in CardOne"
            :key="index"
            :items="items"/>

            <button type="button" class="btn color btn-lg">LEARN MORE</button>
          </div>
        </div>
        <div class="col-6 ms-2 ">
          <div class="row ">
            <div 
              v-for="(image , index) in imgRecepies" 
              :key="index" 
              class="col-6">
              <img 
                :src="image.img"
                class="image" 
              >
            </div>
          </div>
         

        </div>
      </div>
    </div>
    <div class="right"></div>
  </div>
</template>

<style lang="scss" scoped>
@use "../../sass/partials/variabiles.scss" as *;

.text {
  text-align: center;
  width: 40%;
  h4 {
    padding: 20px;
  }

  p {
    padding-bottom: 30px;
  }
}

.mycontainer {
  width: 100%;
  background-color: $white;
  padding-bottom: 35px;

  

  .color {
    background-color: $orange;
    color: $white;
    border-radius: 0;
    margin: 30px 30px;
  }
}

.image{
  width: 270px;
  margin-bottom: 30px;
}
</style>