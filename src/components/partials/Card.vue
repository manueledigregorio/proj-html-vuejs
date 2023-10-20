<script>
export default {
    name:'Card',

    props:{
      cards:Object,
    }
}
</script>

<template>
   <div class="card border-0  pt-3 text-center " style="width: 18rem;">
      <img :src="cards.image" class="card-img-top" :alt="cards.text">
      <h4 class="font" >{{ cards.text }} </h4>
      <p class="color">{{ cards.data }}</p>
  </div>  
</template>

<style lang="scss" scoped>
@use '../../sass/partials/variabiles.scss' as *;
 
  .color{
    color: $lightblack;
  }
</style>