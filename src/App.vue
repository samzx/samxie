<template>
  <div id="app">
    <Hero/>
    <a id="products"/>
    <Products/>
    <Exit />
    <Footer />
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
  color: blue;
  text-decoration: none;
}

a.disabled {
  color: grey;
}

a:hover {
  cursor: pointer;
}

a.disabled:hover {
  color: grey;
  cursor: not-allowed;
}

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin: 0px auto;
  padding-top: 50px;
  padding-bottom: 100px;
  max-width: 1080px;
  background: #eee;
}

.title {
  font-size: 4em;
}

.main {
  padding: 50px 150px;
}

@media only screen and (max-width: 600px) {
  .title {
    font-size: 3em;
  }
  .main {
    padding: 50px 20px;
  }
}

</style>
