<template>
  <div id="app">
    <infinite-slide-bar :barStyle="{ background: '#42b883', padding: '5px 0' }">
      <span style="color: #fff;">Helo World, I love Vue Infinite Slide Bar</span>
    </infinite-slide-bar>
    <infinite-slide-bar :barStyle="{ background: '#42b883', padding: '5px 0' }">
      <img src="http://icons.iconarchive.com/icons/graphicloads/100-flat/256/home-icon.png">
      <img src="http://icons.iconarchive.com/icons/graphicloads/100-flat/256/home-icon.png">
      <img src="http://icons.iconarchive.com/icons/graphicloads/100-flat/256/home-icon.png">
      <img src="http://icons.iconarchive.com/icons/graphicloads/100-flat/256/home-icon.png">
      <img src="http://icons.iconarchive.com/icons/graphicloads/100-flat/256/home-icon.png">
      <img src="http://icons.iconarchive.com/icons/graphicloads/100-flat/256/home-icon.png">
      <img src="http://icons.iconarchive.com/icons/graphicloads/100-flat/256/home-icon.png">
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
