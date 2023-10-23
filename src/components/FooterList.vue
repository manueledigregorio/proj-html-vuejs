<script>
import header from "../data/header";
import icon from "../data/partials/icon";
export default {
  name: "FooterList",
  data() {
    return {
      header,
      icon,
    };
  },
};
</script>

<template>
  <div class="container">
    <div class="row container-custom">


      <div class="line col-3">
        <img src="public/avada-food-logo-mob-2x-200x87.png" alt="logo" />
        <ul class="d-flex mt-5">
          <li class=" icon" v-for="(items, index) in icon" :key="index">
            <a v-if="items.check !== null" :href="items.href">
              <i :class="items.brand"></i>
            </a>
          </li>
        </ul>
      </div>



      <div class="info col-3 line">
        <ul class="d-flex ms-5 flex-column">
          <li class="col-custom pb-4" v-for="(item, i) in header" :key="i">
            <a v-if="item.text !== 'Home'" :href="item.href">{{ item.text }}</a>
          </li>
        </ul>
      </div>



      <div class="col-3 line">
        <div class="contact">
            <h6>CONTACT</h6>
          <ul>
            <li class="d-flex ">
              <i class="fa-solid fa-location-dot"></i>
              <div class="location ">
                <a href="#">775 New York, Ave, Brooklyn, Kings, New York 11203</a>
              </div>
            </li>
            <li class="d-flex">
              <i class="fa-solid fa-phone-flip"></i>
              <p>+ 0100-505-0000</p>
            </li>
            <li>
              <i class="fa-solid fa-envelope"></i>
              <a href="#">info@your-domain.com</a>
            </li>
          </ul>
        </div>
       
      </div>



      <div class="download col-3"> 
        <h6>GET OUR APP!</h6>
        <img src="public/download-android-200x66.png" alt="download-android">
        <img src="public/download-app-store-200x66.png" alt="download-app">
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "../sass/partials/variabiles.scss" as *;

h6{
  color: $orange;
  letter-spacing: 0.3rem;
}

ul{

  padding: 0;
  margin: 0;

  i{
    color: $greey;
    padding-right: 15px;
    font-size: 1.1rem;
  }
}

.line{

  border-right: 1px solid gainsboro;
}

.social{

  padding-right: 10px;
}

.info{
  a{
    color: $black;
    font-size: 1.1rem;
  }
}

.container-custom{
  margin: 70px 0;
}
  .contact{
    padding-left: 40px;
    padding-right: 50px;

    h6{

      padding-bottom: 45px;
    }

    li{
      padding-bottom: 30px;
      a,
      p{
        color: $lightblack;
      }
    }
   
  }

  .download{
    padding-left: 20px;
    img{
      margin-bottom: 10px;
    }

    h6{
      padding-bottom: 30px;
    }
   
  }
</style>