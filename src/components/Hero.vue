<template>
  <div class="hero main">
    <div class="left">
      <h1 class="title">Sam Xie</h1>
      <h1>I'm an <i>Indie maker</i></h1>
      <p>I design, develop and launch new products.</p>
      <p>Fully bootstrapped and fully independant.</p>
    </div>
    <div class="right">
      <div class="image"></div>
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
  flex: 1.61;
  min-width: 300px;
  margin: 20px;
}

.right {
  flex: 1;
  min-width: 300px;
  min-height: 300px;
  margin: 20px;
  position: relative;
}

.image {
  position: absolute;
  height: 100%;
  width: 100%;
  background-color: #21D4FD;
  background-image: linear-gradient(19deg, #21D4FD 0%, #B721FF 100%);
  animation-name: example;
  animation-duration: 4s;
  animation-iteration-count: infinite;
  animation-direction: alternate;
  animation-timing-function: ease-in-out;
}

@keyframes example {
  0%   {transform: translateY(-10px);}
  100% {transform: translateY(10px);}
}

@media only screen and (max-width: 600px) {
  .left, .right {
    margin-left: 0;
    margin-right: 0;
  }
}

</style>
