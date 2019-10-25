<template>
  <AppContainer class="app-container--hero">
    <div class="hero-container">
      <div class="hero main">
        <div class="left">
          <h1 class="title">Hey, I'm Sam.</h1>
          <h1>
          </h1>
          <h2>I design, develop and launch new products.</h2>
          <h2><a href="/#products" class="link">Check out my projects below.</a></h2>
        </div>
        <div class="right">
          <Disk/>
        </div>
      </div>
    </div>
  </AppContainer>
</template>

<script>
import AppContainer from './AppContainer'
import Disk from './Disk'
export default {
  name: "Hero",
  components: {
    AppContainer,
    Disk
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#title {
  font-size: 4em;
}

.link {
  color: #4e6f90;
}

.app-container--hero {
  /* background: linear-gradient(0deg, #fafafa, #fafafa); */
  background: #fafafa;
}

.hero-container {
  height: 100vh;
  max-height: 800px;
  min-height: 600px;
  display: flex;
  justify-content: center;
  flex-direction: column;
}

.hero {
  display: flex;
  flex-wrap: wrap;
}

.left {
  flex: 1;
  min-width: 300px;
}

.right {
  flex: 1;
  min-width: 300px;
  min-height: 250px;
  margin: 30px;
  position: relative;
  display: flex;
  justify-content: center;
  flex-direction: column;
}

@media only screen and (max-width: 600px) {
  .hero-container {
    /* height: auto; */
  }

  .left,
  .right {
    margin-left: 0;
    margin-right: 0;
  }

  h2 {
    font-size: 1.25em;
  }

  .right {
    /* padding-bottom: 100px; */
  }

  .hero {
    padding-top: 25px;
    padding-bottom: 25px;
  }
}
</style>
