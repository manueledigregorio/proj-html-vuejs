<script>
import heroCard from '../../data/partials/heroCard'
export default {
  name:'Hero',
  data() {
    return {
      heroCard
    }
  },
}
</script>

<template>
  <div class="content-hero">    
    <div class="hero d-flex justify-content-center align-content-center   ">
      <div class="title-hero  text-center " >
      <h1 class="text">
          Food Corner: Top japanese <br>
          Restaurant for sushi
        </h1>
        <p class="text">March 25, 2019</p>

        <div class="title">
          <h5>TODAY'S PICK</h5>
        </div>
      </div>
    </div>
    <div class="container  ">
      <div class=" pt-4  my-container position-relative">

        <div class="line-text">
          <div class=" left-text"><hr></div>
          <div class="center-text mx-5 "><h4>FOODIE JOURNAL</h4></div>
          <div class="right-text"><hr></div>
        </div>

        <div  class=" d-flex justify-content-between  px-5">
          <div v-for="(items, index) in heroCard" :key="index" class="card border-0  text-center " style="width: 18rem;">
            <img :src="items.image" class="card-img-top" :alt="items.text">
              <h4 >{{ items.text }} </h4>
              <p >{{ items.data }}</p>
          </div>
        </div>
      </div>

      

        
    </div>
      
  </div>
  
</template>

<style lang="scss" scoped>
@use '../../sass/partials/variabiles.scss' as *;
 
.content-hero{

    .hero{
      background-size: cover;
      background-position: center;
      background-image: url('/hero-big.jpg');
      padding: 185px;
    
    .title-hero{
      background-color: $white;
      border-radius: 10px;
      padding: 50px 90px 30px 90px;
      position: relative;
     

      p{
        color: $lightblack;
      }

     h1{
      margin-bottom: 20px;
     }

     .title{
      background-color: $orange;
      position: absolute;
      top: -20px;
      left: 50%;
      transform: translateX(-50%);
      border-radius: 5px;
      padding: 5px 20px 0px 20px;

      h5{
        color: $white;
        font-size: 0.9rem;
      }

     }
    }

    .text{
      font-family: 'Vidaloka', sans-serif;

    }
  }
  .my-container {
    bottom: 40px;
    background-color: $white;

    hr{
      width: 407px;
    }

  }

  .line-text{
    display: flex;
    align-items: center;
    justify-content: center;
    text-align: center;
    
  }
}
  


  
</style>