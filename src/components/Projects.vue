<script lang='ts'>
   import ProjectComp from './ProjectComp.vue'
   import { Swiper, SwiperSlide } from 'swiper/vue';
   import { Autoplay ,Navigation, Pagination, Scrollbar, A11y } from 'swiper/modules';
   import 'swiper/scss';

   import 'swiper/css/pagination';
   import 'swiper/css/navigation';

   export default {
      components: {
         Swiper,
         SwiperSlide,
         ProjectComp,
      },
      setup() {
         return {
            modules: [Autoplay, Navigation, Pagination, Scrollbar, A11y],
         };
      },
   };
</script>
<template>
   <main>
      <div class="text">
         <h1 class="titleText"> Projects </h1>
      </div>
      <swiper class="swiper"
         :modules="modules"
         :speed="1000"
         :space-between="20"
         navigation
         :loop="true"
         :pagination="{clickable: true}"
         :autoplay="{
            delay: 99999999999,
            disableOnInteraction: false,
            pauseOnMouseEnter: true
         }"
      >
         <swiper-slide class="swiper-slide">
            <a href="https://lonely43.github.io/project-from-figma/">
               <ProjectComp>
                  <template v-slot:title> WheelWidget </template>
                  <template v-slot:summary> Project from freelancee </template>
                  <template v-slot:img> <img loading="lazy" class="img" src="../assets/projects/wheelWidget.png" alt="wheelWidget"> </template>
               </ProjectComp>
            </a>
         </swiper-slide>
         <swiper-slide class="swiper-slide">
            <a href="https://github.com/lonely43/vue-tic-tac-toe">
               <ProjectComp>
                  <template v-slot:title> Tic-Tac-Toe </template>
                  <template v-slot:summary> Tic-tac-toe game made on vue frameWork (not build) </template>
                  <template v-slot:img> <img loading="lazy" class="img" src="../assets/projects/vue-tic-tac-toe.png" alt="wheelWidget"> </template>
               </ProjectComp>
            </a>
         </swiper-slide>
         <swiper-slide class="swiper-slide">
            <a href="https://lonely43.github.io/drawings-shop/">
               <ProjectComp>
                  <template v-slot:title> Drawings shop </template>
                  <template v-slot:summary> One-page web site for single artist </template>
                  <template v-slot:img> <img loading="lazy" class="img" src="../assets/projects/draw-shop.png" alt="wheelWidget"> </template>
               </ProjectComp>
               </a>
         </swiper-slide>
         <swiper-slide class="swiper-slide">
            <a href="https://lonely43.github.io/about.me/">
               <ProjectComp>
                  <template v-slot:title> Old about page </template>
                  <template v-slot:summary> One-page web site for testing my skills (noob) </template>
                  <template v-slot:img> <img loading="lazy" class="img" src="../assets/projects/old-about.png" alt="wheelWidget"> </template>
               </ProjectComp>
            </a>
         </swiper-slide>
      </swiper>
   </main>
</template>
<style lang="scss" scoped>
   *{
      --swiper-pagination-color: black;
      --swiper-pagination-left: auto;
      --swiper-pagination-right: 8px;
      --swiper-pagination-bottom: 8px;
      --swiper-pagination-top: auto;
      --swiper-pagination-fraction-color: inherit;
      --swiper-pagination-progressbar-bg-color: rgba(0, 0, 0, 0.25);
      --swiper-pagination-progressbar-size: 4px;
      --swiper-pagination-bullet-size: 8px;
      --swiper-pagination-bullet-width: 8px;
      --swiper-pagination-bullet-height: 8px;
      --swiper-pagination-bullet-inactive-color: #000000;
      --swiper-pagination-bullet-inactive-opacity: 0.2;
      --swiper-pagination-bullet-opacity: 1;
      --swiper-pagination-bullet-horizontal-gap: 4px;

      --swiper-navigation-size: 44px;
      --swiper-navigation-top-offset: 50%;
      --swiper-navigation-sides-offset: 10px;
      --swiper-navigation-color: rgba(0, 0, 0, 0.795);
   }

   main{
      min-height: 100dvh;

      display: flex;
      flex-direction: column;
      justify-content: space-evenly;

      .swiper{
         max-width: 60%;

         .swiper-slide{
            padding-bottom: 2rem;
            display: flex;
            align-items: center;
            justify-content: center;
         }
      }

      .img{
         width: 320px;
         height: 180px;
         text-align: center;
         border-radius: 0.6rem;
      }
   }

   @media screen and (max-width: 1200px) {
      .swiper{
         max-width: 100% !important;
      }
   }
</style>
