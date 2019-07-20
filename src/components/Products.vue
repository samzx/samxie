<template>
  <AppContainer class="app-container--products">
  <div class="products main">
    <h1 class="title">Here's what I've been up to.</h1>
    <div v-for="(product, index) in products" :key="`product-${index}`">
      <Product v-bind:product="product"/>
    </div>
    <div>
      <p class="more">
        <a href="https://github.com/samzx" class="linked">More on Github</a>
      </p>
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
.more {
  display: flex;
}

.linked {
  margin: auto;
  margin-bottom: 10px;
  padding: 5px 5px;
  color: #4e6f90;
  display: inline-block;
  transition: all 0.3s;
  position: relative;
}

.linked::after {
  width: 0%;
  content: "";
  height: 1px;
  background: #4e6f90;
  position: absolute;
  left: 0;
  bottom: 0;
  transition: width 0.3s;
}

.linked:hover::after {
  width: 100%;
}

.app-container--products {
  background: linear-gradient(0deg, #f8f8f8, #fff);
  /* background: #fafafa; */
}
</style>
