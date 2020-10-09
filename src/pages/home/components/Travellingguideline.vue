<template>
  <div>
    <div class="title">旅游攻略</div>
    <div class="btn">
      <button style="margin-right: 0.08rem;" :class="{btn1: btn1,btn1Active : btn1Active}" @click="goBtn1">趣味亲子游</button>
      <button :class="{btn1: btn2,btn1Active : btn2Active}" @click="goBtn2">旅拍也要出大片</button>
    </div>
    <transition name="guideline">
      <components :is="comp"></components>
    </transition>
    <div class="more-message">
      更多特惠门票 >
    </div>
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
import goodList5 from './goodList5'
import goodList6 from './goodList6'
export default {
  name: 'HomeRecommend',
  data () {
    return {
      comp: 'goodList5',
      btn1: false,
      btn1Active: true,
      btn2Active: false,
      btn2: true
    }
  },
  props: {
    list: Array
  },
  components: {
    goodList5,
    goodList6
  },
  methods: {
    goBtn1 () {
      this.comp = 'goodList5'
      this.btn1Active = true
      this.btn1 = false
      this.btn2 = true
      this.btn2Active = false
    },
    goBtn2 () {
      this.comp = 'goodList6'
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
  .guideline-enter
    transform translateX(-50px)
    opacity 0
    position absolute
  .guideline-leave-to
    transform translateX(50px)
    position absolute
    opacity 0
  .guideline-enter-active,
  .guideline-leave-active
    transition all 1s ease
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
  .more-message
    width 92%
    height 0.88rem
    margin 0 auto
    font-size: 0.28rem
    margin-top: .3rem
    margin-bottom: 0.4rem
    border-radius .08rem
    color #00d0d4
    border 1px solid #00d0d4
    line-height 0.88rem
    text-align center
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
