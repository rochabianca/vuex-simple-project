<template>
  <div
    class="product-list product-list-two col-lg-5 col-md-12 col-sm-12  col-sm-12 mr-lg-5 mb-md-5 mt-sm-5"
  >
    <h2 class="text-center my-4">Product List two</h2>
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
  </div>
</template>

<script>
export default {
  computed: {
    products() {
      return this.$store.state.products;
    },
    saleProducts() {
      return this.$store.getters.saleProducts;
    }
  }
};
</script>

<style lang="scss" scoped></style>
