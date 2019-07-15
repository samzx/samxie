<template>
  <div id="app">
    <Hero/>
    <a id="products"/>
    <Products/>
    <Exit />
  </div>
</template>

<script>
import Hero from './components/Hero.vue'
import Products from './components/Products.vue'
import Exit from './components/Exit.vue'

export default {
  name: 'app',
  components: {
    Hero,
    Products,
    Exit
  }
}
</script>

<style>
body {
  margin: 0;
}

a {
  color: #2c3e50;
  text-decoration: none;
}

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin: 0px auto;
  padding-top: 50px;
  padding-bottom: 100px;
  line-height: 1.4;
  /* background: #eee; */
}

.title {
  font-size: 3em;
}

.main {
  padding: 50px 150px;
}

@media only screen and (max-width: 600px) {
  .title {
    font-size: 3em;
  }
  .main {
    padding: 20px 20px;
  }
  #app {
    padding-top: 0;
    padding-bottom: 0;
  }
}

</style>
