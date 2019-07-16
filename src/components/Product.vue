<template>
  <div class="product">
    <div class="left">
      <a v-if="hasLink(product)" class="icon" v-bind:href="getUrl(product)" v-bind:style="`background-image: url(${product.icon})`"></a>
      <a v-else class="icon disabled" v-bind:style="`background-image: url(${product.icon})`"></a>
    </div>
    <div class="right">
      <h1><a v-bind:href="getUrl(product)">{{product.name}}</a></h1>
      <!-- <img class="screenshots" v-bind:src="product.image" alt=""> -->
      <!-- <div class="tags" v-for="(tag, index) in product.tags" :key="`product-tag-${index}`">{{tag}}</div> -->
      <div v-for="(description, index) in product.descriptions" :key="`product-desctiption-${index}`">
        <p>{{description}}</p>
      </div>
      <div class="links">
        <div v-for="(link, index) in product.links" :key="`product-link-${index}`" class="link">
          <a v-if="link.url" v-bind:href="link.url" class="button linked">{{link.name}}</a>
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
  box-shadow: -5px 5px 20px 2px rgba(0,0,0,0.1);
  margin: 0.67em auto;
  font-size: 2em;
  transition: box-shadow 0.3s, transform 0.3s;
  background-color: white;
  background-image: linear-gradient(19deg, #21D4FD 0%, #B721FF 100%);
  text-align: center;
  color:white;
  font-weight: 900;
  display: block;
  background-size: cover;
  background-position: center;
}

.icon:hover {
  box-shadow: -5px 5px 5px 2px rgba(0,0,0,0.1);
}

.product {
  display: flex;
  flex-wrap: wrap;
  margin: 60px 20px;
}

.left {
  flex: 1;
  min-width: 150px;
}

.right {
  flex: 4;
  min-width: 200px;
}

.links {
  margin-left: -5px;
}

.link {
  display: inline-block;
}

.button {
  margin-right: 10px;
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

.disabled {
  color: grey;
}

.disabled:hover {
  color: grey;
  cursor: not-allowed;
}

.screenshots {
  width: 100%;
  margin: 20px auto;
  box-shadow: 0 0 20px 20px rgba(0,0,0,0.02);
}

.tags{
  display: inline-block;
  box-shadow: 0 0 0px 1px rgba(0,0,0,0.1);
  margin-right: 10px;
  padding: 5px;
  border-radius: 5px;
  font-family: monospace;
}
</style>
