<template>
  <div class="goods-list">
    <div class="goods-item">
      <img class="goods-img"
           src="http://img1.qunarzz.com/sight/p0/2009/27/27c0cfa011a2eb3ba3.water.jpg_256x160_d17a56d9.jpg" alt="">
      <p class="desc-content">长隆野生动物世界</p>
      <p class="price">￥239</p>
    </div>
    <div class="goods-item">
      <img class="goods-img"
           src="http://img1.qunarzz.com/sight/p0/2009/7e/7e0ace460a447ad0a3.water.jpg_256x160_ab373e54.jpg" alt="">
      <p class="desc-content">长隆欢乐世界</p>
      <p class="price">￥97</p>
    </div>
    <div class="goods-item">
      <img class="goods-img"
           src="http://img1.qunarzz.com/sight/p0/201403/04/abf9d2133fbfc65ac5d7d15eebebd374.jpg_256x160_926aa4f1.jpg"
           alt="">
      <p class="desc-content">锦绣中华民俗村</p>
      <p class="price">￥193.5</p>
    </div>
    <div class="goods-item">
      <img class="goods-img"
           src="http://img1.qunarzz.com/sight/p0/1807/f3/f3a998c29724c22aa3.water.jpg_256x160_23f3118d.jpg" alt="">
      <p class="desc-content">古龙峡玻璃大峡谷</p>
      <p class="price">￥93</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'goodList3'
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .goods-list
    display flex
    flex-wrap wrap
    padding-left .20rem
    padding-right .20rem
    justify-content space-between

    .goods-item
      width: 49%
      margin-bottom .20rem
      border-radius .08rem
      overflow hidden

      .goods-img
        width: 100%

      .desc-content
        font-size 0.30912rem
        color #333333
        padding .12rem
        ellipsis()

      .price
        padding-left .065rem
        font-weight bold
        font-size .39744rem
        color #ff7400
</style>
