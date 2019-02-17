<template>
  <div class="product-list-one">
    <h2>Product List One</h2>
    <ul>
      <li v-for="(product, index) in saleProducts" :key="index">
        <span class="name">{{ product.name }} </span>
        <span class="price">${{ product.price }}</span>
      </li>
    </ul>
    <button @click="reducePrice(4)">Reduce Price</button>
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

<style lang="scss" scoped>
.product-list-one {
  background: #4e65f6;
  box-shadow: 1px 2px 3px rgba(0, 0, 0, 0.2);
  margin-bottom: 30px;
  padding: 10px 20px;
}
.product-list-one ul {
  padding: 0;
}
.product-list-one li {
  display: inline-block;
  margin-right: 10px;
  margin-top: 10px;
  padding: 20px;
  background: #9fa6e3;
}
.price {
  font-weight: bold;
  color: white;
}
</style>
