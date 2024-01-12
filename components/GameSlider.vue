
<template>
  <swiper
    :modules="[EffectCards]" effect="cards"
    :slides-per-view="3"
    :space-between="20"
    @swiper="onSwiper"
    @slideChange="onSlideChange"
    class="max-w-lg"
  >
    <swiper-slide>Slide 1</swiper-slide>
    <swiper-slide>Slide 2</swiper-slide>
    <swiper-slide>Slide 3</swiper-slide>
    <swiper-slide>Slide 4</swiper-slide>
    <swiper-slide>Slide 5</swiper-slide>
  </swiper>
</template>


  

<script>
  // Import Swiper Vue.js components
  import { EffectCards } from 'swiper/modules';
  import { Swiper, SwiperSlide } from 'swiper/vue';

  // Import Swiper styles
  import 'swiper/css';

  export default {
    components: {
      Swiper,
      SwiperSlide,
    },
    setup() {
      const onSwiper = (swiper) => {
        console.log(swiper);
      };
      const onSlideChange = () => {
        console.log('slide change');
      };
      return {
        onSwiper,
        onSlideChange,
        EffectCards,
      };
    },
  };
</script>
