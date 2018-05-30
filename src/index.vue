<template>
  <div class="overview--container">
    <div class="overview--slide">
      <div class="coin-overview--container">
        <div class="coin-overview--li-box" v-for="i in 5" :key="i">
          <img class="coin-overview--coin-img" src="https://s2.coinmarketcap.com/static/img/coins/32x32/1.png">
          <div class="coin-overview--coin-box">
            <div class="coin-overview--coin-name">
              Bitcoin (BTC)
            </div>
            <div class="coin-overview--coin-detail">
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
.coin-overview--container {
  float: left;
  width: 50%;
  display: flex;
  justify-content: space-between;
}
.coin-overview--li-box {
  float: left;
  padding: 0 20px;
}
.coin-overview--coin-img {
  float: left;
  margin-top: 5px;
  width: 32px;
  height: 32px;
}
.coin-overview--coin-box {
  float: left;
  padding-left: 10px;
}
.coin-overview--coin-name {
  font-weight: bold;
}
.coin-overview--coin-detail {
  font-size: 11px;
}

@keyframes moveSlideshow {
  100% { 
    transform: translateX(-50%);  
  }
}
.overview--container {
  transform: translate3d(0, 0, 0); /* Hey browser, use your GPU */
  height: 60px;
  background-color: #ffffff;
  box-shadow: 0 1px 0 0 rgba(0, 0, 0, 0.06);
  margin-bottom: 20px;
  position: relative;
  padding: 10px;
  overflow: hidden;
}
.overview--slide {
  transform: translate3d(0, 0, 0); /* Hey browser, use your GPU */
  height: 50px;
  width: 200%;
  position: absolute;
  top: 10px;
  left: 0;
  animation: moveSlideshow 12s linear infinite !important;
}
</style>
