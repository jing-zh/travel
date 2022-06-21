<template>
  <swiper :options="swiperOption" v-if="showSwiper">
    <!-- slides -->
    <swiper-slide v-for="item of list" :key="item.id"
      ><img class="swiper-img" :src="item.imgUrl"
    /></swiper-slide>
    <!-- Optional controls -->
    <div class="swiper-pagination" slot="pagination"></div>
  </swiper>
</template>

<script>
import { computed } from "vue";

export default {
  name: "HomeSwiper",
  props: {
    list: Array,
  },

  setup(props) {
    const swiperOption = {
      pagination: ".swiper-pagination",
      loop: true,
    };
    const showSwiper = computed(() => {
      return props.list.length;
    });
    return { swiperOption, showSwiper };
  },
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
