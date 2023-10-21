<script>
export default {
 name:'BigCard',

 data() {
  return {
    
  }
 },
 props:{
   items: Object,

 }
  
}

</script>

<template>
  
  <div class="cards">
    <div>
      <img :src="items.img" alt="" />
    </div>
    <div class="p-4">
        <h4 class="font">{{ items.title }}</h4>
        <p class=" p-2 ">{{ items.subtitle }}</p>
        <hr>
        <p>{{ items.description }}</p>
          
        
    </div>
  </div>
  
</template>

<style lang="scss" scoped>

img {
    width: 100%;
  }




</style>
