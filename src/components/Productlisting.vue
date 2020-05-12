<template>
  <div class="main-container">
    <h3>
      {{animal.animal_name}}
      <span
        style="color: forestgreen; font-size: 25px; margin-left: 1rem"
      >{{"$" + animal.price}}</span>
    </h3>
    <img :src="animal.image" class="homepageImg" />
    <div class="buttons">
      <button>Learn More</button>
      <button>Add to Cart</button>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    animal: Object
  }
};
</script>

<style scoped>
.main-container {
  width: 20%;
  padding: 1rem;
}
.homepageImg {
  height: 200px;
  width: 200px;
  object-fit: cover;
  border: 3px solid black;
}
h3 {
}
button {
  width: 30%;
}
.buttons {
  width: 100%;
  display: flex;
  justify-content: space-around;
}
button {
  border-radius: 1rem;
  background-color: rgb(147, 233, 107);
  border: none;
  padding: 0.5rem 1rem;
}
</style>