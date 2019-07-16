<template>
  <AppContainer class="app-container--products">
  <div class="products main">
    <h1 class="title">Here's what I've been up to.</h1>
    <div v-for="(product, index) in products" :key="`product-${index}`">
      <Product v-bind:product="product"/>
    </div>
  </div>
  </AppContainer>
</template>

<script>
import Product from './Product.vue'
import AppContainer from './AppContainer'
import products from '../data/products'

export default {
  name: 'Products',
  components: {
    Product,
    AppContainer
  },
  data: () => ({
    products
  })
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.app-container--products {
  background: linear-gradient(0deg, #f8f8f8, #fff);
  /* background: #fafafa; */
}
</style>
