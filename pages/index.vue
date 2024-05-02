<template lang="">
   <main class="main">
      <app-breadcrumbs :path="[{}]" />
      <home-hero-section />
   </main>
</template>
<script setup>
import appBreadcrumbs from "@/components/ui/appBreadcrumbs.vue";
import homeHeroSection from "@/components/sections/homeHeroSection.vue";
</script>
<style lang=""></style>
