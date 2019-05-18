<template>
  <div class="product">
    <div class="left">
      <div class="icon">

      </div>
    </div>
    <div class="right">
      <h1>{{product.name}}</h1>
      <div v-for="(description, index) in product.descriptions" :key="`product-desctiption-${index}`">
        <p>{{description}}</p>
      </div>
      <div class="links">
        <div v-for="(link, index) in product.links" :key="`product-link-${index}`" class="link">
          <a v-if="link.url" v-bind:href="link.url" target="_blank">{{link.name}}</a>
          <a v-else class="disabled">{{link.name}}</a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Product',
  props: {
    product: Object,
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.icon {
  height: 45px;
  width: 45px;
  border-radius: 5px;
  box-shadow: -5px 5px 5px 2px rgba(0,0,0,0.1);
  margin: 0.67em auto;
  font-size: 2em;
  transition: box-shadow 0.3s;
  background-color: #21D4FD;
  background-image: linear-gradient(19deg, #21D4FD 0%, #B721FF 100%);
}

.icon:hover {
  box-shadow: 0 0 5px 2px rgba(0,0,0,0.1);
}

.product {
  display: flex;
  flex-wrap: wrap;
  margin: 80px 20px;
}

.left {
  flex: 1;
  min-width: 150px;
}

.right {
  flex: 4;
  min-width: 200px;
}

.link {
  margin-right: 10px; 
  padding: 5px 10px;
  border-radius: 5px;
  border: 1px solid #ddd;
  display: inline-block;
}
</style>
