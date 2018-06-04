<template>
  <div class="container">
    <div class="slide">
      <div class="list--container" style="background-color: red;color: white;">
        <div>Helo oewjhksajdoskad;lsa;'dsads</div>
      </div>
      <div class="list--container" style="background-color: green;color: white;">
        <div>Helo oewjhksajdoskad;lsa;'dsads</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'vue-infinite-slide-bar',
}
</script>

<style scoped>
.list--container {
  float: left;
  width: 50%;
  height: 60px; /* Can custom */
}

@keyframes moveSlideshow {
  100% { 
    transform: translateX(-50%);  
  }
}
.container {
  transform: translate3d(0, 0, 0); /* Hey browser, please use my GPU */
  height: 60px; /* Can custom */
  background-color: #ffffff;
  box-shadow: 0 1px 0 0 rgba(0, 0, 0, 0.06); /* Can custom */
  position: relative;
  overflow: hidden;
}
.slide {
  transform: translate3d(0, 0, 0); /* Hey browser, please use my GPU */
  width: 200%;
  animation: moveSlideshow 12s linear infinite !important; /* Can custom */
}
</style>
