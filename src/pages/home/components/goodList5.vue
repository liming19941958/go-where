<template>
  <div class="goods-list">
    <div class="goods-item">
      <img class="goods-img" src="http://tr-osdcp.qunarzz.com/tr-osd-tr-manager/img/7d9b233c71cad13ded0013f9c9cec635.jpg" alt="">
      <p class="desc-content">驾一叶扁舟，寻瓯江往事</p>
    </div>
    <div class="goods-item">
      <img class="goods-img" src="http://tr-osdcp.qunarzz.com/tr-osd-tr-manager/img/fd16ccffb2e2376ff370bda3bebebd71.jpg" alt="">
      <p class="desc-content">不负嵊夏好时光，泗乎太安逸</p>
    </div>
    <div class="goods-item">
      <img class="goods-img" src="http://tr-osdcp.qunarzz.com/tr-osd-tr-manager/img/c2ae82fcc9fa11fa253e5919c49bcfbf.jpg" alt="">
      <p class="desc-content">含往返飞机票(含税)+3晚住宿探访日本</p>
    </div>
    <div class="goods-item">
      <img class="goods-img" src="http://tr-osdcp.qunarzz.com/tr-osd-tr-manager/img/5a11974656794b4715156501be10c1b7.jpg" alt="">
      <p class="desc-content">厦门，带娃出行与幸福同行</p>
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
</style>
