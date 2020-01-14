<template>
  <div>
    <div class="app-container">
      <slot></slot>
    </div>
  </div>
  
</template>

<script>
export default {
  name: 'AppContainer',
}
</script>

<style scoped>
.app-container {
  max-width: 1080px;
  margin: auto;
}
</style>
