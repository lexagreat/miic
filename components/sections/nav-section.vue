<template lang="">
   <section class="home-navigation">
      <div class="container">
         <ul class="home-navigation__list">
            <li>
               <nuxt-link
                  data-scroll="experience"
                  class="home-navigation__link btn active"
                  >Опыт работы</nuxt-link
               >
            </li>
            <li>
               <nuxt-link
                  data-scroll="services"
                  class="home-navigation__link btn"
                  >Услуги</nuxt-link
               >
            </li>
            <li>
               <nuxt-link data-scroll="team" class="home-navigation__link btn"
                  >Специалисты IT</nuxt-link
               >
            </li>
            <li>
               <nuxt-link data-scroll="cases" class="home-navigation__link btn"
                  >Кейсы</nuxt-link
               >
            </li>
            <li>
               <nuxt-link
                  data-scroll="partners"
                  class="home-navigation__link btn"
                  >Партнеры</nuxt-link
               >
            </li>
         </ul>
      </div>
   </section>
</template>
<script setup>
useNavigation();
</script>
<style lang=""></style>
