<template>
  <div id="app">
    <Hero/>
    <a id="products"/>
    <Products/>
    <Exit/>
  </div>
</template>

<script>
import Hero from './components/Hero'
import Products from './components/Products'
import Exit from './components/Exit'

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
  padding-bottom: 100px;
  line-height: 1.4;
}

.title {
  font-size: 3em;
}

.main {
  padding: 50px 150px;
}

@media only screen and (max-width: 600px) {
  .title {
    font-size: 2.5em;
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
