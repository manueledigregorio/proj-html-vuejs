<script>
export default {
    name:'Card',

    props:{
      cards:Object,
    }
}
</script>

<template>
  <div class="card elemento border-0 pt-3 text-center" style="width: 18rem;">
    <div class="hover-container">
      <img :src="cards.image" class="img-hover card-img-top" :alt="cards.text">
     
      <div class="hover-text d-flex flex-column">
        <div class="link">
          <a :href="cards.href">
            <i class=" d-flex justify-content-center align-items-center " :class="cards.link"></i>
          </a>
        </div>
        {{ cards.text }}
      </div>
    </div>
    <div class="card-body">
      <h4 class="font">{{ cards.text }}</h4>
      <p class="color">{{ cards.data }}</p>
    </div>
  </div>
</template>



<style lang="scss" scoped>
  @use '../../sass/partials/variabiles.scss' as *;
 
  .color{
    color: $lightblack;
  }
  
  .hover-container {
  position: relative;
  overflow: hidden;
}

.hover-container .img-hover {
  width: 100%;
  height: 100%;
  transition: filter 0.5s;
  border-radius: 0;
}

.hover-container .hover-text {
  position: absolute;
  top: 0;
  left: 0;
  align-items: center;
  justify-content: center;
  display: flex;
  background: linear-gradient( transparent, rgba(255, 87, 31, 0.6) , rgba(255, 87, 31, 1));
  background-color: rgba(255, 87, 31, 0.5);
  color: #fff;
  padding: 10px;
  opacity: 0;
  transition: opacity 0.5s;
  width: 100%;
  height: 100%;
}

.hover-container:hover .hover-text {
  opacity: 1;
}

i{
  width: 40px;
  height: 40px;
  background-color: $white;
  border-radius: 50%;
  color: rgba(1, 0, 0, 0.488) ;
}

</style>