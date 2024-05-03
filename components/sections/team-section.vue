<template lang="">
   <section class="home-team section">
      <div class="home-team__wrapper section__wrapper">
         <h2 class="home-team__title h2">Наши специалисты IT</h2>
         <div class="home-team__main">
            <swiper
               slides-per-view="auto"
               :space-between="12"
               :breakpoints="{
                  '993': {
                     slidesPerView: 4,
                     spaceBetween: 20,
                  },
               }"
            >
               <swiper-slide class="team-member" v-for="item in 4" :key="item">
                  <div class="team-member__wrapper">
                     <div class="team-member__image">
                        <img src="@/assets/img/home/team-member.png" alt="" />
                     </div>
                     <ul class="team-member__roles">
                        <li style="z-index: 2">ведущий</li>
                        <li style="z-index: 1">програмист</li>
                     </ul>
                  </div>
                  <div class="team-member__name">
                     Коловалов Никита Станиславович
                  </div>
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
