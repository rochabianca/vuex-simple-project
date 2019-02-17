<template>
  <div id="app">
    <ProductListOne :products="products"></ProductListOne>
    <ProductListTwo :products="products"></ProductListTwo>
  </div>
</template>

<script>
import ProductListOne from "@/components/ProductListOne";
import ProductListTwo from "@/components/ProductListTwo";
export default {
  name: "app",
  components: {
    ProductListOne,
    ProductListTwo
  },
  data() {
    return {
      products: [
        { name: "Banana Skin", price: 20 },
        { name: "Shiny Star", price: 40 },
        { name: "Red Shells", price: 80 }
      ]
    };
  }
};
</script>

<style lang="scss">
body {
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen,
    Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
  color: #fff;
  background: #dddee6;
}
</style>
