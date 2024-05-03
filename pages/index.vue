<template lang="">
   <main class="main">
      <app-breadcrumbs :path="[{}]" />
      <home-hero-section />
      <nav-section />
      <home-experience-section />
      <cases-section />
      <sale-banner />
      <faq-section />
   </main>
</template>
<script setup>
import appBreadcrumbs from "@/components/ui/appBreadcrumbs.vue";
import homeHeroSection from "~/components/sections/home-hero-section.vue";
import navSection from "~/components/sections/nav-section.vue";
import homeExperienceSection from "@/components/sections/homeExperienceSection.vue";
import casesSection from "~/components/sections/cases-section.vue";
import saleBanner from "~/components/sections/sale-banner.vue";
import faqSection from "~/components/sections/faq-section.vue";
</script>
<style lang=""></style>
