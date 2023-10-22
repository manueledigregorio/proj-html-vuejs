<script>
  import icon from '../data/partials/icon.js'
  import header from '../data/header';
export default {
  name:'Header',

  data() {
    return {
      icon,
      header

    }
  },
}
</script>

<template>
  <header>
      <div class="container">
          <div class=" top-header pt-3 d-flex justify-content-between  ">

              <div class="left">
                  <a href="#">Download App </a>
                  <span>iOS</span>
             
                  <a href="#">Advertize with us</a>
              </div>

              <div class="right">
                <div  >
                  <ul class=" d-flex " >
                    <li v-for="(items , index) in icon" :key="index">
                      <a v-if="items.check !== null" :href="items.href">
                        <i :class="items.brand"></i>
                      </a>
                      </li>
                  </ul> 
                </div>
              </div>

          </div>

          <div class=" text-center  ">
            <img src="/avada-food-logo.png" alt="logo">
          </div>

          <div class=" bar-header pt-4 d-flex justify-content-center ">
            <ul class=" d-flex ">
              <li v-for="(item, i) in header" :key="i" >
                <a :href="item.href">{{ item.text }}</a>
              </li> 
            </ul>
            <i class="fa-solid fa-magnifying-glass"></i>
          </div>
          
      </div>
  </header>
</template>

<style lang="scss" scoped>
@use '../sass/partials/variabiles.scss' as *;
@use '../sass/partials/general.scss' as *;
@use'../sass/partials/typography.scss' as *;

header{
  height: 250px;
  background-color: $white;

  .left a{
    color: $greey;
    font-size: 0.8rem;
    

  }

  .left span{
    color: $white;
    padding: 3px 5px;
    background-color: $orange;
    border-radius: 4px;
    font-size: 0.8rem;
    margin-right: 25px;
    
  }

  .right i {
    color: $greey;
    padding-left: 30px;
  }

  .bar-header a{
    color: $black;
    margin-right: 85px;

    &:active{
    color: $orange;
    padding-bottom: 10px;
    border-bottom: 3px solid $orange ;
    }
  }
  

}
</style>
