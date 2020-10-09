<template>
  <div class="goods-list">
    <div class="goods-item">
      <img class="goods-img" src="http://tr-osdcp.qunarzz.com/tr-osd-tr-manager/img/6ff48e0e00432f823bf593deec6d3397.jpg" alt="">
      <p class="desc-content">美帝的美，留在图里也要藏在心底</p>
    </div>
    <div class="goods-item">
      <img class="goods-img" src="http://tr-osdcp.qunarzz.com/tr-osd-tr-manager/img/729fced755d522ccfc280ef155f45518.jpg" alt="">
      <p class="desc-content">在秘密花园，领略意大利风情</p>
    </div>
    <div class="goods-item">
      <img class="goods-img" src="//tr-osdcp.qunarzz.com/tr-osd-tr-manager/img/e86b37fef48851353d6f5ae0090cc974.jpg" alt="">
      <p class="desc-content">带着相机去旅行，圆一场青海梦</p>
    </div>
    <div class="goods-item">
      <img class="goods-img" src="http://tr-osdcp.qunarzz.com/tr-osd-tr-manager/img/24d074328b5a26845ebb92be20b38754.jpg" alt="">
      <p class="desc-content">陪你去三亚，陪你去天涯海角</p>
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
