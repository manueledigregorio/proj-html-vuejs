<script>
export default {
  name:'PopularText'
}
</script>

<template>

<div class=" container-popular w-100 d-flex ">
  <div class=" d-flex p-3 justify-content-center  align-items-center popular w-50">
    <p class="font">Popular</p>
  </div>
  <div class="d-flex p-3 justify-content-center align-items-center w-50">
    <p class="font">Recent</p>
  </div>
</div>
  
</template>

<style lang="scss" scoped>
@use "../../sass/partials/variabiles.scss" as *;

.container-popular{
  border: 1px solid gainsboro;

  .popular{
    border-right: 1px solid gainsboro;
    text-align: center;
    background-color: $white;
    
  }
    p{
      margin: 0;
      font-size: 1.2rem;


    }
}

</style>