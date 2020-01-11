<template>
  <AppContainer class="app-container--hero">
    <div class="hero-container">
      <div class="hero main">
        <div class="left">
          <div>
            <h1 class="title">Hey, I'm Sam.</h1>
            <h2>I design, develop and launch new products.</h2>
            <h2><a href="/#products" class="link">Check them out below.</a></h2>
          </div>
        </div>
        <div class="right image-container">
          <img class="image" src="https://res.cloudinary.com/xielabs/image/upload/v1575374644/dark-gradient.svg" />
        </div>
      </div>
    </div>
  </AppContainer>
</template>

<script>
import AppContainer from './AppContainer'
export default {
  name: "Hero",
  components: {
    AppContainer
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.image-container {
  margin: 10px;
  height: 300px;
  width: 332px;
}
.image {
  max-height: 300px;
  max-width: 100%;
}
#title {
  font-size: 4em;
}

.link {
  color: #2b79a8;
}

.app-container--hero {
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
  min-width: 320px;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.right {
  flex: 1;
  min-width: 320px;
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
