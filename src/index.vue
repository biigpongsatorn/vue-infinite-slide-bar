<script>
export default {
  name: 'vue-infinite-slide-bar',
  props: {
    barStyle: Object,
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
    }
  },
  computed: {
    customStyle () {
      return {
        ...this.barStyle,
        'animation-duration': this.duration,
        'animation-direction': this.direction,
        'animation-delay': this.delay
      }
    }
  },
  render (createElement) {
    const bar = createElement('div', { class: 'vifnslb-bar' }, this.$slots.default)
    return createElement('div', { class: ['vifnslb-container'], style: this.customStyle }, [bar, bar])
  }
}
</script>

<style scoped>
@keyframes moveSlideshow {
  100% {
    transform: translateX(-50%);
  }
}
.vifnslb-container {
  transform: translate3d(0, 0, 0); /* Hey browser, please use my GPU */
  position: relative;
  overflow: hidden;
  animation-name: moveSlideshow;
  animation-iteration-count: infinite;
  animation-timing-function: linear;
  display: flex;
  width: max-content;
  min-width: 200%;
}
.vifnslb-bar {
  width: 50%;
}
</style>
