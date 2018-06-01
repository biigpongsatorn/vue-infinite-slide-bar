<template>
  <div class="container">
    <div class="slide">
      <div class="list--container">
        <div class="list--li-box" v-for="i in 5" :key="i">
          <img class="list--coin-img" src="https://s2.coinmarketcap.com/static/img/coins/32x32/1.png">
          <div class="list--coin-box">
            <div class="list--coin-name">
              Bitcoin (BTC)
            </div>
            <div class="list--coin-detail">
              $16,815.10 
              <span class="has-text-success">(11.68%)</span>
            </div>
          </div>
        </div>
      </div>
      <div class="list--container">
        <div class="list--li-box" v-for="i in 5" :key="i">
          <img class="list--coin-img" src="https://s2.coinmarketcap.com/static/img/coins/32x32/1.png">
          <div class="list--coin-box">
            <div class="list--coin-name">
              Bitcoin (BTC)
            </div>
            <div class="list--coin-detail">
              $16,815.10 
              <span class="has-text-success">(11.68%)</span>
            </div>
          </div>
        </div>
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
  display: flex;
  justify-content: space-between;
}
.list--li-box {
  float: left;
  padding: 0 20px;
}
.list--coin-img {
  float: left;
  margin-top: 5px;
  width: 32px;
  height: 32px;
}
.list--coin-box {
  float: left;
  padding-left: 10px;
}
.list--coin-name {
  font-weight: bold;
}
.list--coin-detail {
  font-size: 11px;
}

@keyframes moveSlideshow {
  100% { 
    transform: translateX(-50%);  
  }
}
.container {
  transform: translate3d(0, 0, 0); /* Hey browser, use your GPU */
  height: 60px;
  background-color: #ffffff;
  box-shadow: 0 1px 0 0 rgba(0, 0, 0, 0.06);
  margin-bottom: 20px;
  position: relative;
  padding: 10px;
  overflow: hidden;
}
.slide {
  transform: translate3d(0, 0, 0); /* Hey browser, use your GPU */
  height: 50px;
  width: 200%;
  position: absolute;
  top: 10px;
  left: 0;
  animation: moveSlideshow 12s linear infinite !important;
}
</style>
