<template lang="">
   <div class="breadcrumbs">
      <div class="container">
         <ul class="breadcrumbs__list">
            <li>
               <nuxt-link to="/" class="breadcrumbs__link">Главная</nuxt-link>
            </li>
            <li v-for="link in path" :key="link">
               <nuxt-link :to="link.to" class="breadcrumbs__link">{{
                  link.name
               }}</nuxt-link>
            </li>
         </ul>
      </div>
   </div>
</template>
<script setup>
const props = defineProps({
   path: Array,
});
</script>
<style lang=""></style>
