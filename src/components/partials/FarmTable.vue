<script>
import BigCard from "./BigCard.vue";
import { CardTwo } from "../../data/partials/bigCard";
export default {
  name: "FarmTable",
  data() {
    return {
      CardTwo,
    };
  },
  components: {
    BigCard,
  },
};
</script>

<template>
  <div class="container">
    <div class="title">
      <div class=" w-50"> 
        <h4>FARM TO TABLE</h4>
        <p>
          Lorem ipsum dolor sit amet consectetur, adipisicing elit. Atque laborum
          qui ut maiores, tempore id nihil facilis minus quaerat doloribus!
        </p>
      </div>
      
      <div class=" blog  float-end  position-relative ">
        <a  href="#"
          >READ OUR BLOG
          <i class="fa-solid fa-book-open-reader"></i>
        </a>
      </div>
    </div> 
      <div class="row w-100 ">
        <div class="col-8">
          <div class="mycontainer">
          <BigCard
            v-for="(items, index) in CardTwo"
            :key="index"
            :items="items"
          />
          <div class="px-4 d-flex justify-content-between">
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
      
        <div class="col-4">

          <div class=" container-right ms-4">
            <div class="image-bg">
              <div class="cont-text text-center ">
                <h5>VIEW OUR 
                    LATEST 
                    RECIPES
                </h5>
              </div>
            </div>
          </div>
         
        </div>
      </div>

  </div>
</template>

<style lang="scss" scoped>
@use "../../sass/partials/variabiles.scss" as *;
.container {
  margin-top: 150px;
  .blog{
    bottom: 70px;
    
    i {
    font-size: 0.9em;
    }

    a {
      border-radius: 2px;
      padding: 10px 25px;
      color: $white;
      background-color: $orange;
    }
  }
  

  .mycontainer {
    width: 100%;
    background-color: $white;
    padding-bottom: 20px;
    margin-top: 80px;

    a {
      color: $lightblack;
      margin-right: 5px;

      i {
        font-size: 0.6em;
      }
    }
  }


  .image-bg {
    background-image: url(public/ad-bg.jpg);
    background-size: cover;
    background-position: center;
    height: 410px;
    width: 100%; /* Imposta la larghezza al 100% */
    margin-top: 80px;

    .cont-text{
      width: 100%;
      height: 100%;
      padding: 160px 120px;

      h5{
        line-height: 1.9rem;
      }
    }
  }
}
</style>