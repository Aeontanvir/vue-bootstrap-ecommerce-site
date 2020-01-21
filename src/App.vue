<template>
  <div id="app">
    <navbar></navbar>
    <div class="container main-container">
      <div class="row">
        <div class="col-sm-9">
          <invertory :items="items" @newItemAdded="addCartItem"></invertory>
        </div>
        <div class="col-sm-3">
          <cart :items="cart" @removeCartItem="removeFromCart"></cart>
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
      items: [],
      cart: []
    };
  },
  mounted() {
    this.items = data;
  },
  methods: {
    addCartItem(item) {
      this.cart.push(item);
    },
    removeFromCart(index) {
      this.cart.splice(index, 1);
    }
  }
};
</script>

<style>
.main-container {
  padding-top: 20px;
}
</style>
