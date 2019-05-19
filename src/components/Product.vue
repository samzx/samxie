<template>
  <div class="product">
    <div class="left">
      <a v-if="hasLink(product)" class="icon" v-bind:href="getUrl(product)"></a>
      <a v-else class="icon disabled"></a>
    </div>
    <div class="right">
      <h1>{{product.name}}</h1>
      <div v-for="(description, index) in product.descriptions" :key="`product-desctiption-${index}`">
        <p>{{description}}</p>
      </div>
      <div class="links">
        <div v-for="(link, index) in product.links" :key="`product-link-${index}`" class="link">
          <a v-if="link.url" v-bind:href="link.url" target="_blank" class="button">{{link.name}}</a>
          <a v-else class="button disabled">{{link.name}}</a>
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
  methods: {
    open: (url) => {
      window.open(url)
    },
    hasLink: (product) => {
      return product.links.map(link => link.url).filter(url => url != undefined).length > 0
    },
    getUrl: (product) => {
      const firstLink = product.links[0]
      return firstLink ? firstLink.url : '/'
    }
  }
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
  text-align: center;
  color:white;
  font-weight: 900;
  display: block;
}

.icon:hover {
  box-shadow: 0 0 5px 2px rgba(0,0,0,0.1);
}

.disabled {
  cursor: not-allowed;
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
  display: inline-block;
}

.button {
  margin-right: 10px; 
  padding: 5px 10px;
  border-radius: 5px;
  border: 1px solid #ddd;
  display: inline-block;
  transition: all 0.3s;
}

</style>
