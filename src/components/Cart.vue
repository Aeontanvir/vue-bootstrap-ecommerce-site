<template>
  <ul class="list-group">
    <li class="list-group-item">Product - Price</li>
    <hr />
    <li class="list-group-item" v-for="(item, index) in items" :key="index">
      <span class="float-left">{{item.title}} - {{item.price}}</span>
      <span class="float-right">
        <button class="btn btn-sm btn-outline-danger" @click="removeItem(index)">x</button>
      </span>
    </li>
    <hr v-if="items.length" />
    <li class="list-group-item">Total - {{totalPrice}}</li>
  </ul>
</template>

<script>
export default {
  props: ["items"],
  computed: {
    totalPrice() {
      var total = 0;
      this.items.forEach(element => {
        total += parseFloat(element.price);
      });
      return total;
    }
  },
  methods: {
    removeItem(index) {
      this.$emit("removeCartItem", index);
    }
  }
};
</script>

<style>
</style>