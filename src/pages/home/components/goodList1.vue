<template>
  <div class="goods-list">
    <div class="goods-item">
      <img class="goods-img" src="http://imgs.qunarzz.com/p/p3/1809/e5/59de4bd338291802.jpg_256x160_98c152cd.jpg" alt="">
      <p class="desc-content">含往返火车票+5晚住宿</p>
      <p class="price">￥2457</p>
    </div>
    <div class="goods-item">
      <img class="goods-img" src="http://imgs.qunarzz.com/p/p45/1809/22/d815539e74dc4a02.jpg_256x160_00a6f984.jpg" alt="">
      <p class="desc-content">含往返飞机票(含税)+4晚住宿</p>
      <p class="price">￥2233</p>
    </div>
    <div class="goods-item">
      <img class="goods-img" src="http://imgs.qunarzz.com/p/p19/1809/b9/2a3d362aabcbb02.jpg_256x160_28907832.jpg" alt="">
      <p class="desc-content">含往返飞机票(含税)+3晚住宿</p>
      <p class="price">￥2150</p>
    </div>
    <div class="goods-item">
      <img class="goods-img" src="http://imgs.qunarzz.com/p/p70/1809/e7/4941057a6aae702.jpg_256x160_9fee6ccb.jpg" alt="">
      <p class="desc-content">含往返飞机票(含税)+4晚住宿</p>
      <p class="price">￥2676</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'goodList1'
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
