<template>
  <div>
    <home-header></home-header>
    <home-swiper></home-swiper>
    <home-icons></home-icons>
    <special-holiday></special-holiday>
    <more-special-holiday></more-special-holiday>
    <special-tickets></special-tickets>
    <more-special-tickets></more-special-tickets>
    <travelling-guideline></travelling-guideline>
  </div>
</template>

<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
import HomeIcons from './components/Icons'
import SpecialHoliday from './components/Specialholiday'
import SpecialTickets from './components/Specialtickets'
import TravellingGuideline from './components/Travellingguideline'
import MoreSpecialHoliday from './components/MoreSpecialHoliday'
import MoreSpecialTickets from './components/MoreSpecialtickets'
import axios from 'axios'
import { mapState } from 'vuex'
export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcons,
    SpecialHoliday,
    SpecialTickets,
    TravellingGuideline,
    MoreSpecialHoliday,
    MoreSpecialTickets
  },
  data () {
    return {
      lastCity: '',
      iconList: [],
      recommendList: [],
      weekendList: []
    }
  },
  computed: {
    ...mapState(['city'])
  },
  methods: {
    getHomeInfo () {
      axios.get('/api/index.json?city=' + this.city)
        .then(this.getHomeInfoSucc)
    },
    getHomeInfoSucc (res) {
      res = res.data
      if (res.ret && res.data) {
        const data = res.data
        this.swiperList = data.swiperList
        this.iconList = data.iconList
        this.recommendList = data.recommendList
        this.weekendList = data.weekendList
      }
    }
  },
  mounted () {
    this.lastCity = this.city
    this.getHomeInfo()
  },
  activated () {
    if (this.lastCity !== this.city) {
      this.lastCity = this.city
      this.getHomeInfo()
    }
  }
}
</script>

<style>

</style>
