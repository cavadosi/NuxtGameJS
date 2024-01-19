<template>
  <swiper
  :effect="'cards'"
  :grabCursor="true"
  :modules="modules"
  class="mySwiper relative"
  >
  <swiper-slide>Slide 1</swiper-slide>
  <swiper-slide>Slide 2</swiper-slide><swiper-slide>Slide 3</swiper-slide>
  <swiper-slide>Slide 4</swiper-slide><swiper-slide>Slide 5</swiper-slide>
  <swiper-slide>Slide 6</swiper-slide><swiper-slide>Slide 7</swiper-slide>
  <swiper-slide>Slide 8</swiper-slide><swiper-slide>Slide 9</swiper-slide>
  <div class="gooey absolute -inset-x-12 -inset-y-10 "></div>
  </swiper>
</template>

<script>
  // Import Swiper Vue.js components
  import { Swiper, SwiperSlide } from 'swiper/vue';

  // Import Swiper styles
  import 'swiper/css';

  import 'swiper/css/effect-cards';



  // import required modules
  import { EffectCards } from 'swiper/modules';

  export default {
    components: {
      Swiper,
      SwiperSlide,
    },
    setup() {
      return {
        modules: [EffectCards],
      };
    },
  };
</script>

<style scoped>
.swiper {
  width: 240px;
  height: 320px;
}

.swiper-slide {
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 18px;
  font-size: 22px;
  font-weight: bold;
  color: #fff;
}

.swiper-slide:nth-child(1n) {
  background-color: rgb(206, 17, 17);
}

.swiper-slide:nth-child(2n) {
  background-color: rgb(0, 140, 255);
}

.swiper-slide:nth-child(3n) {
  background-color: rgb(10, 184, 111);
}

.swiper-slide:nth-child(4n) {
  background-color: rgb(211, 122, 7);
}

.swiper-slide:nth-child(5n) {
  background-color: rgb(118, 163, 12);
}

.swiper-slide:nth-child(6n) {
  background-color: rgb(180, 10, 47);
}

.swiper-slide:nth-child(7n) {
  background-color: rgb(35, 99, 19);
}

.swiper-slide:nth-child(8n) {
  background-color: rgb(0, 68, 255);
}

.swiper-slide:nth-child(9n) {
  background-color: rgb(218, 12, 218);
}

.swiper-slide:nth-child(10n) {
  background-color: rgb(54, 94, 77);
}

.gooey{
  background-image: linear-gradient(120deg, #22c55e 0%, #15803d 100%);
  border-radius: 42% 58% 70% 30% / 45% 45% 55% 55%;
  max-width: 400px; max-height: 450px;
  animation: morph 10s linear infinite; 
  transform-style: preserve-3d;
  outline: 1px solid transparent;
  will-change: border-radius;
}
.gooey:before,
.gooey:after{
  content: '';
  width: 100%;
  height: 100%;
  display: block;
  position: absolute;
  left: 0; top: 0;
  border-radius: 42% 58% 70% 30% / 45% 45% 55% 55%;
  box-shadow: 5px 5px 89px #041A29;
  will-change: border-radius, transform, opacity;
  animation-delay: 200ms;
  background-image: linear-gradient(120deg, #16a34a 0%, #14532d 100%);
}

.gooey:before{
  animation: morph 3s linear infinite;
  opacity: .21;
  animation-duration: 1.5s;
}

.gooey:after{
  animation: morph 3s linear infinite;
  animation-delay: 400ms;
  opacity: .89;
  content: "";
  line-height: 120px;
  text-indent: -21px;
}

@keyframes morph{
  0%,100%{
  border-radius: 42% 58% 70% 30% / 45% 45% 55% 55%;
    transform: translate3d(0,0,0) rotateZ(0.01deg);
  }
  34%{
      border-radius: 70% 30% 46% 54% / 30% 29% 71% 70%;
    transform:  translate3d(0,5px,0) rotateZ(0.01deg);
  }
  50%{
    opacity: .89;
    transform: translate3d(0,0,0) rotateZ(0.01deg);
  }
  67%{
    border-radius: 100% 60% 60% 100% / 100% 100% 60% 60% ;
    transform: translate3d(0,-3px,0) rotateZ(0.01deg);
  }
}

@keyframes fadeIn{
  100%{
    transform: scale(1.03);
    opacity: 0;
  }
}
</style>