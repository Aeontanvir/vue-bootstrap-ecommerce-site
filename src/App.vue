<template>
  <div id="app">
    <navbar></navbar>
    <div class="container">
      <div class="row">
        <div class="col-sm-9">
          <invertory></invertory>
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
export default {
  components: {
    Navbar,
    Invertory,
    Cart
  }
};
</script>

<style>
.container {
  padding-top: 20px;
}
</style>
