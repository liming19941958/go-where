<template>
  <div :class="{mainBox: mainBox,mainBoxActive : mainBoxActive}">
    <div class="title">特惠度假</div>
    <div class="btn">
       <button style="margin-right: 0.08rem;" :class="{btn1: btn1,btn1Active : btn1Active}" @click="goBtn1">当季热门度假</button>
       <button :class="{btn1: btn2,btn1Active : btn2Active}" @click="goBtn2">今日特惠度假</button>
    </div>
    <transition name="holiday">
      <components :is="comp"></components>
    </transition>
<!--    <ul>-->
<!--      <router-link-->
<!--        tag="li"-->
<!--        class="item border-bottom"-->
<!--        v-for="item of list"-->
<!--        :key="item.id"-->
<!--        :to="'/detail/' + item.id"-->
<!--      >-->
<!--        <img class="item-img" :src="item.imgUrl" />-->
<!--        <div class="item-info">-->
<!--          <p class="item-title">{{item.title}}</p>-->
<!--          <p class="item-desc">{{item.desc}}</p>-->
<!--          <button class="item-button">查看详情</button>-->
<!--        </div>-->
<!--      </router-link>-->
<!--    </ul>-->
  </div>
</template>

<script>
import goodList1 from './goodList1'
import goodList2 from './goodList2'
export default {
  name: 'HomeRecommend',
  data () {
    return {
      comp: 'goodList1',
      btn1: false,
      btn1Active: true,
      btn2Active: false,
      btn2: true,
      mainBox: true,
      mainBoxActive: false
    }
  },
  props: {
    list: Array
  },
  components: {
    goodList1,
    goodList2
  },
  methods: {
    goBtn1 () {
      this.comp = 'goodList1'
      this.mainBox = true
      this.mainBoxActive = false
      this.btn1Active = true
      this.btn1 = false
      this.btn2 = true
      this.btn2Active = false
    },
    goBtn2 () {
      this.comp = 'goodList2'
      this.mainBox = false
      this.mainBoxActive = true
      this.btn1Active = false
      this.btn1 = true
      this.btn2 = false
      this.btn2Active = true
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .holiday-enter
    transform translateX(-50px)
    opacity 0
    position absolute
  .holiday-leave-to
    position absolute
    opacity 0
    transform translateX(50px)
  .holiday-enter-active,
  .holiday-leave-active
    transition all 1.5s ease
  .mainBoxActive
    height 8.7rem
    transition: all .6s ease-out
  .mainBox
    height 8.4rem
    transition: all .6s ease-out
  .title
    margin-top: .2rem
    line-height: .8rem
    text-indent: .2rem
    color #1d1d1d
    font-weight: bold
    font-size: .36rem
  .btn
    margin-top -2px
    margin-bottom  5px
    line-height: .8rem
    padding-left: .4rem
    .btn1
      height: .6582rem
      padding 0 10px
      color #666666
      background-color: transparent
      border: 1px solid #d7d7d7
      border-radius .07rem
    .btn1Active
      height: .6582rem
      padding 0 10px
      border: 1px solid #17c0c8
      border-radius .07rem
      color #fff
      background-color: #17c0c8

  .item
    overflow: hidden
    display: flex
    height: 1.9rem
    .item-img
      width: 1.7rem
      height: 1.7rem
      padding: .1rem
    .item-info
      flex: 1
      padding: .1rem
      min-width: 0
      .item-title
        line-height: .54rem
        font-size: .32rem
        ellipsis()
      .item-desc
        line-height: .4rem
        color: #ccc
        ellipsis()
      .item-button
        line-height: .44rem
        margin-top: .16rem
        background: #ff9300
        padding: 0 .2rem
        border-radius: .06rem
        color: #fff
</style>
