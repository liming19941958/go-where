<template>
  <div class="goods-list">
    <div class="goods-item">
      <img class="goods-img" src="http://imgs.qunarzz.com/vs_ceph_b2c_001/3b7913bd-79cd-40a2-ba1f-65b8a7909f62.jpg_180x120x90_ad8c6608.jpg" alt="">
      <p class="desc-content">驻马店-丽江 8天跟团游</p>
      <p class="price">￥2280</p>
    </div>
    <div class="goods-item">
      <img class="goods-img" src="http://imgs.qunarzz.com/vs_ceph_vs_tts/e5d3f0c8-de53-47db-94cf-d804248c5cc7.jpg_180x120x90_04207df7.jpg" alt="">
      <p class="desc-content">驻马店-大理 6天跟团游</p>
      <p class="price">￥2376</p>
    </div>
    <div class="goods-item">
      <img class="goods-img" src="http://imgs.qunarzz.com/vs_ceph_vs_tts/5c35e45c-ef6b-4d7b-8019-d980747fffd3.jpg_180x120x90_e8cea1ec.jpg" alt="">
      <p class="desc-content">驻马店-大理 6天跟团游</p>
      <p class="price">￥1650</p>
    </div>
    <div class="goods-item">
      <img class="goods-img" src="http://imgs.qunarzz.com/vs_ceph_vs_tts/f46f6a92-7aa6-44c9-a8b6-a34aa9bbb1d0.jpg_180x120x90_5886e280.jpg" alt="">
      <p class="desc-content">驻马店-大理 8天跟团游</p>
      <p class="price">￥2070</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'goodList2'
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
