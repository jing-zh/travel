<template>
  <swiper :options="swiperOption">
    <!-- slides -->
    <swiper-slide v-for="item of swiperList" :key="item.id"
      ><img class="swiper-img" :src="item.imgUrl"
    /></swiper-slide>
    <!-- Optional controls -->
    <div class="swiper-pagination" slot="pagination"></div>
  </swiper>
</template>

<script>
export default {
  name: "HomeSwiper",
  data() {
    return {
      swiperOption: {
        pagination: ".swiper-pagination",
        loop: true
      },
      swiperList: [
        {
          id: "0001",
          imgUrl:
            "https://imgs.qunarzz.com/sight/source/1812/4c/33ad31d025fef.jpg_r_640x214_7821b813.jpg"
        },
        {
          id: "0002",
          imgUrl:
            "https://imgs.qunarzz.com/sight/source/1505/53/4bcd11cc3a5374.jpg_r_640x214_988a4cee.jpg"
        }
      ]
    };
  }
};
</script>

<style lang="stylus" scoped>
>>> .swiper-pagination-bullet-active
        background: #fff
// .wrapper
//     overflow: hidden
//     width: 100%
//     height: 0
//     padding-bottom: 31.25%
     .swiper-img
         width: 100%
</style>
