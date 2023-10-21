<script>
export default {
name: 'Search',
}
</script>

<template>

<div class="search mt-5 d-flex align-items-center justify-content-center">
  <div class="header-center px-3 d-flex align-items-center ">
    <div class="t-search">
      <i class="fa-solid fa-magnifying-glass"></i>
    </div>
    <div class="form-search">
      <input 
        class="form-control custom-input me-2" type="search"
        placeholder="Seach..." aria-label="Search" 
      />
    </div>
  </div>
</div>

  
</template>


<style lang="scss" scoped>

.search {
  background-color: whitesmoke;
  width: 100%;
  height: 50px;

  .header-center {
    background-color: white;
    width: 100%;
    border: 1px solid gainsboro;
    border-radius: 5px;
    padding: 7px;

     i{
      color: #B1B1B1;
    }
  }
  .t-search{
    width: 15%;
    text-align: center;
  }

  .custom-input {
  background-color: white;
  box-shadow: none;
  border: none;
  }
}

</style>