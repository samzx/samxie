<template>
  <div class="exit main">
    <h1 class="title">Perspectives</h1>
    <div class="card">
      <a class="left" href="/blog">
        <div class="text">
          <h1>Blog</h1>
          <p>The journey of an indie maker</p>
        </div>
        <div class="blog-image"></div>
      </a>
      <a class="right" href="https://twitter.com/samxstudio">
        <div class="text">
          <h1>Twitter</h1>
          <p>@samxstudio</p>
        </div>
        <div class="twitter-image"></div>
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Exit'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.card {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-evenly;
  text-align: center;
}

.left:hover, .right:hover {
  box-shadow: 0 0 20px 5px rgba(0,0,0,0.1);
  transform: scale(1.02);
}

.left, .right {
  min-width: 300px;
  height: 300px;
  box-shadow: 0 0 10px 5px rgba(0,0,0,0.05);
  margin: 20px;
  border-radius: 10px;
  transition: box-shadow 0.3s;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  transition: all 0.3s;
}

.text {
  padding: 20px;
}

.blog-image {
  height: 120px;
  width: 100%;
  border-radius: 0 0px 10px 10px;
  background-color: #21D4FD;
  background-image: linear-gradient(19deg, #21D4FD 0%, #B721FF 100%);
  mask: url("https://res.cloudinary.com/xielabs/image/upload/c_scale,w_600/v1559459519/blog-logo.png");
  mask-repeat: no-repeat;
  mask-size: 200px;
  mask-position: 55px 20%;
}

.twitter-image {
  height: 120px;
  width: 100%;
  border-radius: 0 0px 10px 10px;
  background-color: #21D4FD;
  background-image: linear-gradient(19deg, #21D4FD 0%, #B721FF 100%);
  mask: url("https://res.cloudinary.com/xielabs/image/upload/c_scale,w_600/v1559459519/twitter-logo.png");
  mask-repeat: no-repeat;
  mask-size: cover;
  mask-position: 10px 33%;
}

@media only screen and (max-width: 600px) {
  .left, .right {
    margin: 20px;
  }
}
</style>
