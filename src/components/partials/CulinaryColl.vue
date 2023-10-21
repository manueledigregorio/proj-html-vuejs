<script>
import culinary from '../../data/partials/culinary';
export default {
name:'CulinaryColl',
data() {
  return {
    culinary
  }
},
}
</script>

<template>
  <div class="container">
    <div class="d-flex justify-content-center">
      <div class="text">
        <h4>CULINARY COLLECTION</h4>
        <p>
          Aliquam erat volutpat.Ut quis Lorem, ipsum reiciendis iusto,
          blanditiis hic deserunt accusantium ullam mollitia delectus.
        </p>
      </div>
    </div>

    <div class="row">
      <div 
      v-for="(items, index) in culinary"
      :key="index"
       class="col-3 mb-4 ">
        <div class="card-custom">
          <img :src="items.img" alt="">
          <div class=" px-2 w-100 ">
            <a href="">{{ items.text }}</a>
          </div>
        </div>
      </div>
    </div>

  </div>
  
</template>


<style lang="scss" scoped>

@use '../../sass/partials/variabiles.scss' as *;
 
.text {
  text-align: center;
  width: 40%;
  h4{
  padding: 20px;
  }

  p {
    padding-bottom: 30px;
  }
}

.card-custom{
  width: 100%;
  background-color: $white;
  text-align: center;
  padding-bottom: 10px;

  img{
    width: 100px;
  }

  a{
    color: $black;
    display: block;
    width: 100%;
    padding: 10px;
    
  }a:hover{
    background-color: $orange;
    transition: 0.2s;
    color: $white;
  }
}

</style>