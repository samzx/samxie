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
    name: "Final Slash VR",
    icon: "https://res.cloudinary.com/xielabs/image/upload/c_scale,w_90/v1563021446/1.png", 
    descriptions: ["A short survival experience on an abandonded planet."],
    links: [
      {
        name: "Proof of Concept",
        url: "https://samzx.itch.io/final-slash-vr"
      }
    ]
  },
  {
    name: "GradPlanner",
    icon: "https://res.cloudinary.com/xielabs/image/upload/c_scale,w_90/v1563021826/favicon-gradplanner.png",
    descriptions: ["Helping graduating students find jobs."],
    links: [
      {
        name: "Coming Soon"
      }
    ]
  },
  {
    name: "MPHWatch",
    icon: "https://res.cloudinary.com/xielabs/image/upload/c_scale,w_90/v1563022381/mphwatch-icon.png",
    descriptions: ["Stats for cryptocurrency miners mining on Mining Pool Hub.", "Clean and simple interface for monitoring mining activity."],
    links: [
      {
        name: "Login",
        url: "https://mphwatch.samxie.net"
      },
      {
        name: "Demo",
        url: "https://mphwatch.samxie.net/demo"
      },
      {
        name: "Github",
        url: "https://github.com/samzx/mphwatch"
      },
      {
        name: "Retro",
        url: "https://medium.com/@samxie/mphwatch-retrospective-ebf33c070bda"
      }
    ]
  },
  {
    name: "BookIT Maps",
    icon: "https://res.cloudinary.com/xielabs/image/upload/c_scale,w_90/v1563022111/bookitmaps.png",
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
        url: "https://medium.com/@samxie/bookit-maps-retrospective-96c4ec6dd289"
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
