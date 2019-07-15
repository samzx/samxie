<template>
  <AppContainer class="app-container--products">
  <div class="products main">
    <h1 class="title">Products</h1>
    <div v-for="(product, index) in products" :key="`product-${index}`">
      <Product v-bind:product="product"/>
    </div>
  </div>
  </AppContainer>
</template>

<script>
import Product from './Product.vue'
import AppContainer from './AppContainer'

const products = [
  {
    name: "Final Slash VR",
    icon: "https://res.cloudinary.com/xielabs/image/upload/c_scale,w_90/v1560002222/Slash.png",
    descriptions: ["A short survival experience on an abandoned planet."],
    links: [
      {
        name: "Proof of Concept",
        url: "https://samzx.itch.io/final-slash-vr"
      }
    ]
  },
  {
    name: "GradPlanner",
    icon: "https://res.cloudinary.com/xielabs/image/upload/c_scale,w_90/v1563105252/favicon-gradplanner-trans.png",
    descriptions: ["Helping graduating students find jobs."],
    links: [
      {
        name: "Proof of Concept",
        url: "http://gradplanner.samxie.net/"
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
    icon: "https://res.cloudinary.com/xielabs/image/upload/c_scale,w_90/v1563105254/bookitmaps-white.png",
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
  },
  {
    name: "Zendesk Ticket Viewer",
    icon: "https://res.cloudinary.com/xielabs/image/upload/c_scale,w_90/v1563090058/zendesk-cc.jpg",
    descriptions: ["My submission for the Zendesk coding challenge."],
    links: [
      {
        name: "Demo",
        url: "http://zendeskcc.samxie.net/demo"
      },
      {
        name: "Github",
        url: "https://github.com/samzx/zendesk-coding-challenge"
      }
    ]
  }
];

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
  background: linear-gradient(0deg, #f8f8f8, #fff)
}
</style>
