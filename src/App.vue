<template>
  <div
    id="app"
    class="container"
  >
    <div class="row justify-content-center mt-md-5">
      <ProductListOne></ProductListOne>
      <ProductListTwo></ProductListTwo>
    </div>
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
  data () {
    return {};
  }
};
</script>

<style lang="scss">
body {
  font-family: "Montserrat", sans-serif;
  background: #fafcfd;
}
</style>
