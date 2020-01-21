<template>
  <div id="app">
    <navbar></navbar>
    <div class="container">
      <div class="row">
        <div class="col-sm-9">
          <invertory :items="items"></invertory>
        </div>
        <div class="col-sm-3">
          <cart></cart>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Navbar from "./components/Navbar";
import Cart from "./components/Cart";
import Invertory from "./components/Inventory";
import data from "./data.js";
export default {
  components: {
    Navbar,
    Invertory,
    Cart
  },
  data() {
    return {
      items: []
    };
  },
  mounted() {
    this.items = data;
  }
};
</script>

<style>
.container {
  padding-top: 20px;
}
</style>
