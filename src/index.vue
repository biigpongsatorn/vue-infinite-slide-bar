<template>
  <div class="container" :style="barStyle">
    <div v-for="i in 2" :key="i" class="slide-container">
      <slot></slot>
    </div>
  </div>
</template>

<script>
export default {
  name: 'vue-infinite-slide-bar',
  props: {
    duration: {
      type: String,
      default: '12s'
    },
    direction: {
      type: String,
      default: 'normal'
    },
    delay: {
      type: String,
      default: '0s'
    },
    style: {
      type: Object,
      default: { padding: '5px 0' }
    }
  },
  computed: {
    barStyle () {
      return {
        ...this.style,
        'animation-duration': this.duration,
        'animation-direction': this.direction,
        'animation-delay': this.delay
      }
    }
  }
}
</script>

<style scoped>
.slide-container {
  float: left;
  width: 50%;
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
  width: 200%;
  animation-name: moveSlideshow;
  animation-iteration-count: infinite;
  animation-timing-function: linear;
}
</style>
