<script>
export default {
  name: "Form",
};
</script>

<template>
  <div class="container-form">
    <h2 class="font my-4">Subscibe <span>&</span> Recieve A Free eBook</h2>
    <p>
      Lorem ipsum dolor sit, amet consectetur adipisicing elit. Omnis non
      laudantium maiores sit iure ipsum quasi tenetur, nam sequi at.
    </p>
    <div class="d-flex my-5">
      <input type="text" placeholder="insert your mail..." />
      <button type="button" class="color">SUBSCRIBE</button>
    </div>
    <span>Lorem ipsum dolor sit amet.</span>
  </div>
</template>

<style lang="scss" scoped>
@use "../../sass/partials/variabiles.scss" as *;

.container-form {
  background-image: url("/Form-img.png");
  background-color: $white;
  background-size: cover;
  background-position: center;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  margin-top: 110px;
  padding-bottom: 150px;
  padding-top: 100px;

  h2 {
    span {
      color: $orange;
    }
  }

  input {
    border: 1px solid $greey;
    border-radius: 5px;
    padding: 13px 170px;
  }

  .color {
    background-color: $orange;
    color: $white;
    border-radius: 5px;
    margin-left: 30px;
    border: $orange;
    padding: 13px 60px;
  }
}
</style>