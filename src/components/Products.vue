<template>
  <div class="products main">
    <h1 class="title">Products</h1>
    <div v-for="(product, index) in products" :key="`product-${index}`">
      <Product v-bind:product="product"/>
    </div>
  </div>
</template>

<script>
import Product from './Product.vue'

const products = [
  {
    name: "GradPlanner",
    icon: "https://res.cloudinary.com/xielabs/image/upload/c_scale,w_45/v1559457508/gradplanner.png",
    descriptions: ["Helping graduating students find jobs."],
    links: [
      {
        name: "Coming Soon"
      }
    ]
  },
  {
    name: "MPHWatch",
    icon: "https://res.cloudinary.com/xielabs/image/upload/c_scale,w_45/v1559457507/MPHWatch_logo.png",
    descriptions: ["Stats for cryptocurrency miners mining on Mining Pool Hub.", "Clean and simple interface for monitoring mining activity."],
    links: [
      {
        name: "Demo",
        url: "https://mphwatch.samxie.net/demo"
      },
      {
        name: "Live",
        url: "https://mphwatch.samxie.net"
      },
      {
        name: "Github",
        url: "https://github.com/samzx/mphwatch"
      },
      {
        name: "Retro",
        url: "https://www.samxie.net/blog/mphwatch-retrospective/"
      }
    ]
  },
  {
    name: "BookIT Maps",
    icon: "https://res.cloudinary.com/xielabs/image/upload/c_scale,w_45/v1559457508/bookitmaps-logo.png",
    descriptions: ["BookIT Maps guides users to find the location of their bookings through an interactive map."],
    links: [
      {
        name: "Demo",
        url: "http://bookitmaps.samxie.net/demo"
      },
      {
        name: "Github",
        url: "https://github.com/samzx/bookit-maps-front"
      },
      {
        name: "Retro",
        url: "https://www.samxie.net/blog/bookit-maps-retrospective/"
      }
    ]
  }
];

export default {
  name: 'Products',
  components: {
    Product
    },
  data: () => ({
    products
  })
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
