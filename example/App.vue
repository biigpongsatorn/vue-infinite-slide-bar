<template>
  <div id="app">
    <infinite-slide-bar :style="{ color: '#fff', background: '#42b883', 'font-weight': 'bold' }">
      Helo World, I love Vue Infinite Slide Bar
    </infinite-slide-bar>
  </div>
</template>

<script>
import infiniteSlideBar from '../src'

export default {
  name: 'app',
  components: { infiniteSlideBar }
}
</script>

<style>
body {
  margin: 0 !important;
}
</style>
