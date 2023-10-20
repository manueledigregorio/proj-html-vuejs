<script>
export default {
  name:'Hero'
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

  </div>
  
</template>

<style lang="scss" scoped>
@use '../../sass/partials/variabiles.scss' as *;

  .hero{
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


  
</style>