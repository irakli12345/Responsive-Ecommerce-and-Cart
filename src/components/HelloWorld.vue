<template>
  <div style="display: flex">
    <div class="hello">
      <Productlisting v-for="animal in data" :key="generateKey(animal)" :animal="animal"></Productlisting>
    </div>
    <Cart></Cart>
  </div>
</template>

<script>
import Productlisting from "./Productlisting";
import Cart from "./Cart";
export default {
  name: "Helloworld",
  components: {
    Productlisting,
    Cart
  },
  data: function() {
    return { data: null };
  },
  mounted: function() {
    fetch("http://localhost:3000/products")
      .then(res => res.json())
      .then(data => (this.data = data));
  },
  methods: {
    generateKey(sth) {
      sth + Math.random() * 100000;
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
ul {
  list-style-type: none;
  padding: 0;
}

a {
  color: #42b983;
}
* {
  font-family: "Anton";
}
.hello {
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
  width: 70vw;
}
</style>
