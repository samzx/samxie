<template>
  <div class="hero main">
    <div class="left">
      <h1 class="title">Sam Xie</h1>
      <h1>I'm an <i>Indie maker</i></h1>
      <p>I design, develop and launch new products.</p>
      <p>Fully bootstrapped and fully independent.</p>
    </div>
    <div class="right">
      <div class="image">
        <div class="image-background"></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Hero'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
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

.image {
  position: absolute;
  height: 300px;
  width: 100%;
  display: flex;
  justify-content: center;
  /* animation-name: example;
  animation-duration: 4s;
  animation-iteration-count: infinite;
  animation-direction: alternate;
  animation-timing-function: ease-in-out; */
}

.image-background {
  position: absolute;
  width: 100%;
  height: 300px;
  background-color: #21D4FD;
  background-image: linear-gradient(19deg, #21D4FD 0%, #B721FF 100%);
  mask: url(../assets/stroke.png);
  mask-repeat: no-repeat;
  mask-size: contain;
}

.image img {
  margin: auto;
  width: 100%;
  max-width: 300px;
  position: absolute;
}

@keyframes example {
  0%   {transform: translateY(10px);}
  100% {transform: translateY(0px);}
}

@media only screen and (max-width: 600px) {
  .left, .right {
    margin-left: 0;
    margin-right: 0;
  }
}

</style>
