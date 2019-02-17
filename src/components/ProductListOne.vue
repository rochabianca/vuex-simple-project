<template>
  <div
    class="product-list product-list-one col-lg-5 col-md-12 col-sm-12 mr-lg-5 mb-md-5 mb-sm-4"
  >
    <h2 class="text-center my-4 title">Product List One</h2>
    <ul class="m-0 p-0">
      <li
        v-for="(product, index) in saleProducts"
        :key="index"
        class="d-flex justify-content-between mb-3 product-item"
      >
        <span class="name">{{ product.name }} </span>
        <span class="price">${{ product.price }}</span>
      </li>
    </ul>
    <button class="btn btn-block btn-light my-4" @click="reducePrice(4)">
      Reduce Price
    </button>
  </div>
</template>

<script>
import { mapActions, mapGetters } from "vuex";

export default {
  computed: {
    products() {
      return this.$store.state.products;
    },
    ...mapGetters(["saleProducts"])
  },
  methods: {
    ...mapActions(["reducePrice"])
  }
};
</script>

<style lang="scss">
.product-list {
  color: white;
  border-radius: 5px;
  box-shadow: 2px 2px 8px #ddd;
  &.product-list-one {
    background: #0a92f8;
  }
  &.product-list-two {
    background: #57b07c;
  }
  ul {
    list-style: none;
  }
  .product-item {
    background: #fff;
    color: #444;
    padding: 15px;
    border-radius: 3px;
  }
}
</style>
