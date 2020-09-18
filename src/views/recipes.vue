<template>
  <div class="home">
    <HelloWorld msg="Welcome to Your Vue.js App" />
    <div class="row">
      <button class="btn btn-primary">New Recipe</button>
      <br />
      <br />
      <h1>Please Select a Recipe!</h1>
    </div>
    <div class="col-md-6">
      <products />
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import products from "@/components/products.vue";
//import prices from "../json/prices.json";
export default {
  name: "recipes",
  components: {
    products
  }
};
</script>
<style scoped>
.home button {
  margin-top: 20px;
  padding: 15px;
  margin-left: 60px;
  font-weight: bold;
  color: cornsilk;
  font-size: 18px;
  float: left;
  background-color: #42b983;
  border-radius: 5px;
  height: 60px;
}
.home .row h1 {
  margin-bottom: 60px;
  text-align: center;
  margin-left: 380px;
  margin-top: 75px;
  color: darkcyan;
}
</style>
