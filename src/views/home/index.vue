<template>
  <div class="page">
    <swiper :options="bannerOption">
      <swiper-slide v-for="(banner,index) in bannerList"
                    @click.native="changeDesaturate(index)"
                    :key="index"
                    class="banner-slide">
        <img :src="banner.url"
             @click="changeDesaturate(index)">
      </swiper-slide>
    </swiper>
  </div>
</template>
<script>
import 'swiper/dist/css/swiper.css'
import { swiper, swiperSlide } from 'vue-awesome-swiper'
export default {
  name: 'Home',
  components: {
    swiper,
    swiperSlide
  },
  data () {
    return {
      bannerOption: {
        // direction: 'vertical',
        // pagination: {
        //   el: '.swiper-pagination',
        //   clickable: true
        // }
      },
      bannerList: [
        {
          isdesaturate: true,
          url: require('../../../public/img/大沙河片区2.jpg'),
          url1: require('../../../public/img/大沙河片区1.jpg')
        },
        {
          isdesaturate: true,
          url: require('../../../public/img/滨海大道2.jpg'),
          url1: require('../../../public/img/滨海大道1.jpg')
        },
        {
          isdesaturate: true,
          url: require('../../../public/img/福田中心区2.jpg'),
          url1: require('../../../public/img/福田中心区1.jpg')
        },
        {
          isdesaturate: true,
          url: require('../../../public/img/国贸2.jpg'),
          url1: require('../../../public/img/国贸1.jpg')
        }
      ]
    }
  },
  created () {

  },
  mounted () {

  },
  methods: {
    changeDesaturate (index) {
      this.bannerList[index].isdesaturate = false
      switch (index) {
        case 0:
          this.bannerList[index].url = this.bannerList[index].url1

          break
        case 1:
          this.bannerList[index].url = this.bannerList[index].url1

          break
        case 2:
          this.bannerList[index].url = this.bannerList[index].url1

          break
        case 3:
          this.bannerList[index].url = this.bannerList[index].url1

          break
      }
    }
  }
}
</script>
<style lang="less" scoped>
</style>
