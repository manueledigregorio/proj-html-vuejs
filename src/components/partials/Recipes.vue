<script>
import imgRecepies from '../../data/partials/imgRecepies';
export default {
  name: "Recipes",

  data() {
    return {
      imgRecepies
    }
  },
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
            <div class="cards">
              <div>
                <img src="/Yogurt-Nan-600x395.jpg" alt="" />
              </div>
              <div class="p-4">
                <h4 class="font">Lunch favorite with salad Naan And Beans</h4>
                <p class=" p-2 ">Bakery, Featured, Healty, Latest Recipes, Staff Picks</p>
                <hr>
                <p>
                  Lorem ipsum dolor sit, amet consectetur adipisicing elit.
                  Pariatur unde, magnam iure fugit earum nostrum! Cupiditate
                  iste neque nulla saepe, dolor delectus ullam perspiciatis
                  inventore maiores vel aliquam adipisci id quaerat perferendis
                  tenetur atque enim sit hic qui harum facere earum ex accusamus
                  in. Sunt eos minus ducimus unde labore.
                </p>
               
              </div>
            </div>
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

  img {
    width: 100%;
  }

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