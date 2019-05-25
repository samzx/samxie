<template>
  <div class="hero-container">    
    <div class="hero main">
      <div class="left">
        <h1 id="title">Sam Xie</h1>
        <h1>
          <p>Hey, I'm Sam</p>
        </h1>
        <p>I design, develop and launch new products.</p>
        <p>Built organically and handcrafted with love.</p>
      </div>
      <div class="right">
        <div class="right-inner">
          <div class="viewport">
            <div class="rotatable">
              <div class="shadow"></div>
            </div>
          </div>
          <div class="circle">
            <div class="circle-outer"></div>
            <div class="circle-inner"></div>
            <div class="circle-center"></div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Hero"
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#title {
  font-size: 4em;
}

.hero-container {
  height: calc(100vh - 100px);
  max-height: 720px;
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
  min-height: 300px;
  margin: 20px;
  position: relative;
  display: flex;
  justify-content: center;
  flex-direction: column;
}

.right-inner {
  height: 66%;
  width: 100%;
  display: flex;
  justify-content: center;
  position: relative;
}

.circle {
  display: flex;
  justify-content: center;
  animation: hovering 2s ease-in-out infinite alternate-reverse;
}

.circle-center {
  height: 180px;
  width: 180px;
  border-radius: 100px;
  background: white;
  position: absolute;
  top: 30px;
}

.circle-inner {
  height: 210px;
  width: 210px;
  border-radius: 110px;
  background-color: #21d4fd;
  background-image: linear-gradient(30deg, #21d4fd 0%, #b721ff 100%);
  position: absolute;
  top: 15px;
  animation: rotate 2s linear infinite reverse;
  transition: all 1s;
}

.circle-outer {
  height: 240px;
  width: 240px;
  border-radius: 120px;
  background-color: #21d4fd;
  background-image: linear-gradient(-60deg, #21d4fd 0%, #b721ff 100%);
  position: absolute;
  animation: rotate 3s linear infinite;
  transition: all 1s;
}

.viewport {
  perspective: 2000;
  perspective-origin: center;
  position: absolute;
  width: 50px;
  height: 300px;
}

.rotatable {
  transform: rotateX(75deg) translateZ(-300px);
  transform-origin: center;
  transition: all 0.5s;
  position: absolute;
  transform-style: preserve-3d;
}

.shadow {
  height: 50px;
  width: 50px;
  border-radius: 25px;
  position: absolute;
  animation: fade 2s ease-in-out infinite alternate-reverse;
}

@keyframes fade {
  0% {
    background-color: rgba(0, 0, 0, 0.033);
    box-shadow: 0px 0px 66px 66px rgba(0, 0, 0, 0.033);
  }
  100% {
    background-color: rgba(0, 0, 0, 0.066);
    box-shadow: 0px 0px 66px 66px rgba(0, 0, 0, 0.066);
  }
}

@keyframes hovering {
  0% {
    transform: translateY(-10px);
  }
  100% {
    transform: translateY(0px);
  }
}

@keyframes rotate {
  0% {
    transform: rotateZ(0deg);
  }
  100% {
    transform: rotateZ(360deg);
  }
}

@media only screen and (max-width: 600px) {
  .hero-container {
    height: auto;
  }

  .left,
  .right {
    margin-left: 0;
    margin-right: 0;
  }

  .right {
    padding-bottom: 100px;
  }

  .hero {
    padding-top: 25px;
    padding-bottom: 25px;
  }
}
</style>
