<template>
  <div class="goods-list">
    <div class="goods-item">
      <img class="goods-img" src="http://imgs.qunarzz.com/sight/p0/201403/04/abf9d2133fbfc65ac5d7d15eebebd374.jpg_256x144_23de1eab.jpg" alt="">
      <p class="desc-content">锦绣中华民俗村</p>
      <p class="price">￥193.5起</p>
    </div>
    <div class="goods-item">
      <img class="goods-img" src="http://imgs.qunarzz.com/sight/p0/1603/20/208ed6bc971a41cf90.img.jpg_256x144_44a94813.jpg" alt="">
      <p class="desc-content">宝墨园</p>
      <p class="price">￥46.8起</p>
    </div>
    <div class="goods-item">
      <img class="goods-img" src="http://imgs.qunarzz.com/sight/p0/1807/f3/f3a998c29724c22aa3.water.jpg_256x144_e8b1042d.jpg" alt="">
      <p class="desc-content">古龙峡玻璃大峡谷</p>
      <p class="price">￥35起</p>
    </div>
    <div class="goods-item">
      <img class="goods-img" src="http://imgs.qunarzz.com/p/p70/1809/e7/4941057a6aae702.jpg_256x160_9fee6ccb.jpg" alt="">
      <p class="desc-content">珠海长隆海洋王国</p>
      <p class="price">￥296起</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'goodList4'
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .goods-list
    display flex
    flex-wrap wrap
    padding-left .20rem
    padding-right  .20rem
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
