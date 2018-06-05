<template>
  <div id="app">
    <infinite-slide-bar>
      <span>
        Helo World, I love Vue Infinite Slide Bar
      </span>
    </infinite-slide-bar>
    <br>
    <infinite-slide-bar>
      <span>
        The following example uses the value "alternate-reverse" to make the animation run backwards first, then forwards
      </span>
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
