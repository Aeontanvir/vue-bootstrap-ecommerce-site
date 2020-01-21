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
          <a href="#" class="btn btn-primary">Add Product</a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["items"]
};
</script>

<style>
.card {
  margin-top: 10px;
}
</style>