<template>
  <div class="icons">
    <swiper :options="pages.length > 1 ? swiperOption : ''">
      <swiper-slide v-for="(page,index) of pages" :key="index">
        <div class="icon" v-for="item of page" :key="item.id">
          <div class="icon-img">
            <img class="icon-img-content" :src="item.iconUrl" alt="">
          </div>
          <p class="icon-desc">{{item.desc}}</p>
        </div>
      </swiper-slide>
      <div class="swiper-pagination"  slot="pagination" v-show="pages.length > 1"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeIcons',
  data () {
    return {
      iconList: [
        {
          id: '001',
          iconUrl: 'http://s.qunarzz.com/homenode/images/touchheader/hotel.png',
          desc: '酒店'
        },
        {
          id: '002',
          iconUrl: 'http://s.qunarzz.com/homenode/images/touchheader/flight.png',
          desc: '机票'
        },
        {
          id: '003',
          iconUrl: '//s.qunarzz.com/homenode/images/touchheader/train.png',
          desc: '火车票'
        },
        {
          id: '004',
          iconUrl: '//s.qunarzz.com/homenode/images/touchheader/package.png',
          desc: '度假'
        },
        {
          id: '005',
          iconUrl: '//s.qunarzz.com/homenode/images/touchheader/piao.png',
          desc: '景点门票'
        },
        {
          id: '006',
          iconUrl: 'https://picbed.qunarzz.com/f5e5770393d759578962e53ee67798c8.png',
          desc: '海外酒店'
        },
        {
          id: '007',
          iconUrl: 'https://picbed.qunarzz.com/377db8cb2143aebf01869c9baad3d325.png',
          desc: '汽车票船票'
        },
        {
          id: '008',
          iconUrl: 'https://picbed.qunarzz.com/a36d2288f19e54562338f4d8ef986288.png',
          desc: '低价机票'
        },
        {
          id: '009',
          iconUrl: 'https://picbed.qunarzz.com/ae617a31e0bd5803d76918b817f6d942.png',
          desc: '自由行'
        },
        {
          id: '010',
          iconUrl: 'https://picbed.qunarzz.com/1316dc82d1ce6259686d5a68880e5a9d.png',
          desc: '攻略'
        },
        {
          id: '011',
          iconUrl: 'https://picbed.qunarzz.com/01d2f57f920666364197a850dab859a8.png',
          desc: '民宿客栈'
        },
        {
          id: '012',
          iconUrl: 'https://picbed.qunarzz.com/83af731055e121a3251690b225327b56.png',
          desc: '专车自驾'
        },
        {
          id: '013',
          iconUrl: 'https://picbed.qunarzz.com/5b6737be49ca243072ca614f07803b83.png',
          desc: '赚钱▪信用卡'
        },
        {
          id: '014',
          iconUrl: 'https://picbed.qunarzz.com/1e107321f5396ea4994cd832232ecf8a.png',
          desc: '旅游团购'
        },
        {
          id: '015',
          iconUrl: 'https://picbed.qunarzz.com/c65b3bb7571a6bd62df669213e44b84d.png',
          desc: '一日游'
        },
        {
          id: '016',
          iconUrl: 'https://picbed.qunarzz.com/f6bb08a239ce1b038204120a8d1e4669.png',
          desc: '特惠酒店'
        }
      ],
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true,
        autoplay: 4000
      }
    }
  },
  computed: {
    pages () {
      const pages = []
      this.iconList.forEach((item, index) => {
        const page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  @import '~styles/mixins.styl'
  .icons >>> .swiper-container
    height: 0
    padding-bottom: 50%
    margin-top: .1rem
  >>>.swiper-pagination-bullet-active
    background: #c3f0ff
  .swiper-pagination
    bottom: 0px
  .icon
    position relative
    overflow hidden
    float: left
    width: 25%
    height: 0
    padding-bottom: 25%
    .icon-img
      position: absolute
      top: 0
      left: 0
      right: 0
      bottom: .85rem
      .icon-img-content
        height: 100%
        margin 0 auto
        display block
    .icon-desc
      position: absolute
      left: 0
      right: 0
      bottom: 0
      height: .85rem
      line-height: .85rem
      color: #333333
      text-align center
      //超出范围以省略号显示
      ellipsis()
</style>
