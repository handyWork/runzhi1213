<template>
  <div class="download">
    <banner img="../assets/img/appDown.jpg" title="下载APP2"/>

    <div>
      <swiper :options="swiperOption">
        <swiper-slide><img :src="require('../assets/img/toplogo.png')"></swiper-slide>
        <swiper-slide><img :src="require('../assets/img/toplogo.png')"></swiper-slide>
        <swiper-slide><img :src="require('../assets/img/toplogo.png')"></swiper-slide>
        <swiper-slide><img :src="require('../assets/img/toplogo.png')"></swiper-slide>
        <swiper-slide><img :src="require('../assets/img/toplogo.png')"></swiper-slide>
        <div class="swiper-button-next" slot="button-next"></div>
        <div class="swiper-button-prev" slot="button-prev"></div>
      </swiper>
    </div>
  </div>



</template>

<script>

import Banner from "../components/Banner";
import {swiper, swiperSlide} from "vue-awesome-swiper";

export default {
  components: {
    Banner,
    swiper,
    swiperSlide
  },
  data() {
    return {
      swiperOption: {//swiper3
        autoplay: true,
        speed: 1000,
        height: window.innerHeight - 60,
        slidesPerView: 3,
        centeredSlides: false,
        navigation: {
          nextEl: '.swiper-button-next',
          prevEl: '.swiper-button-prev',
        },
      }
    };
  },
};
</script>

<style lang="scss" scoped>
</style>