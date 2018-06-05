<template>
  <div class="container">
    <div class="slide"
      :style="{
        'animation-duration': '12s',
        'animation-direction': false ? 'reverse' : 'normal',
        'animation-delay': '0s'
      }">
      <div v-for="i in 2" :key="i" class="slide-container">
        <slot></slot>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'vue-infinite-slide-bar',
  props: {}
}
</script>

<style scoped>
.slide-container {
  float: left;
  width: 50%;
  padding: 5px 0;
  height: 20px;
  background: #fff7cc;
  color: #f60;
}

@keyframes moveSlideshow {
  100% { 
    transform: translateX(-50%);  
  }
}
.container {
  transform: translate3d(0, 0, 0); /* Hey browser, please use my GPU */
  position: relative;
  overflow: hidden;
}
.slide {
  transform: translate3d(0, 0, 0); /* Hey browser, please use my GPU */
  width: 200%;
  animation-name: moveSlideshow;
  animation-iteration-count: infinite;
  animation-timing-function: linear;
}
</style>
