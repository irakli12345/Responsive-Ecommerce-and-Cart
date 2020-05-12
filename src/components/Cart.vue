<template>
  <div class="cart">
    <Productincart></Productincart>
    <Productincart></Productincart>
    <Productincart></Productincart>
    <Productincart></Productincart>
  </div>
</template>

<script>
import Productincart from "./Productincart";
export default {
  components: {
    Productincart
  }
};
</script>

<style scoped>
.cart {
  flex-grow: 1;
}
</style>