<template lang="">
   <section class="home-partners section">
      <div class="section__wrapper">
         <h2 class="home-partners__title h2">Наши партнеры</h2>
         <div class="home-partners__content">
            <swiper
               :space-between="40"
               slides-per-view="auto"
               :breakpoints="{
                  '993': {
                     spaceBetween: 80,
                  },
               }"
            >
               <swiper-slide class="small">
                  <img src="@/assets/img/home/partners1.png" alt="" />
               </swiper-slide>
               <swiper-slide>
                  <img src="@/assets/img/home/partners2.png" alt="" />
               </swiper-slide>
               <swiper-slide class="small">
                  <img src="@/assets/img/home/partners3.png" alt="" />
               </swiper-slide>
               <swiper-slide>
                  <img src="@/assets/img/home/partners4.png" alt="" />
               </swiper-slide>
               <swiper-slide>
                  <img src="@/assets/img/home/partners5.png" alt="" />
               </swiper-slide>
            </swiper>
         </div>
      </div>
   </section>
</template>
<script setup>
import { Swiper, SwiperSlide } from "swiper/vue";
</script>
<style lang=""></style>
