<script>
import BigCard from "./BigCard.vue";
import { CardTwo } from "../../data/partials/bigCard";
import FarmTableDown from "./FarmTableDown.vue";
import Seach from "./Seach.vue";
import FarmRight from "./FarmRight.vue"
export default {
  name: "FarmTable",
  data() {
    return {
      CardTwo,
    };
  },
  components: {
    BigCard,
    FarmTableDown,
    Seach,
    FarmRight,
  },
};
</script>

<template>
  <div class="container">
    <div class="title">
      <div class="blog float-end">
        <a href="#"
          >READ OUR BLOG
          <i class="fa-solid fa-book-open-reader"></i>
        </a>
      </div>
      <div class="w-50">
        <h4>FARM TO TABLE</h4>
        <p>
          Lorem ipsum dolor sit amet consectetur, adipisicing elit. Atque
          laborum qui ut maiores, tempore id nihil facilis minus quaerat
          doloribus!
        </p>
      </div>
    </div>
    <div class="row w-100">
      <!--COLONNA DI DESTRA 8-->
      <div class="col-8 p-0">
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
        <FarmTableDown />
      </div>
      <!-- CHIUSURA COLONNA DI DESTRA 8-->

      <!--COLONNA DI SINISTRA 4-->  
      <div class="col-4">
        <div class="container-right ms-4">
          <FarmRight />
          <Seach />
        </div>

        
      </div>
      <!-- CHIUSURA COLONNA DI SINISTRA 4-->  


    </div>
   
  </div>
</template>

<style lang="scss" scoped>
@use "../../sass/partials/variabiles.scss" as *;
.container {
  margin-top: 150px;
  .blog {
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
}
</style>