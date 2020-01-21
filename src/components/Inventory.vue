<template>
  <div class="row">
    <div class="col-4" v-for="(item, index) in items" :key="index">
      <div class="card">
        <img :src="item.photo" class="card-img-top" :alt="item.title" />
        <div class="card-body">
          <div class="clearfix">
            <h5 class="card-title float-left">{{item.title}}</h5>
            <h5 class="card-title float-right">{{item.price}}</h5>
          </div>

          <p class="card-text">{{item.description}}</p>
          <button @click="addToCart(item)" class="btn btn-sm btn-outline-info">Add Product</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["items"],
  methods: {
    addToCart(item) {
      this.$emit("newItemAdded", item);
    }
  }
};
</script>

<style>
.card {
  margin-bottom: 10px;
}
</style>