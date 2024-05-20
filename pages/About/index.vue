<template>
   <main class="main">
      <ui-app-breadcrumbs :path="path" />
      <sections-about-hero />
      <sections-experience-section />
      <sections-about-concepts />
      <sections-brief-section />
      <sections-team-section />
      <sections-cases-section />
      <sections-partners-section />
      <sections-sale-banner />
      <sections-faq-section />
      <sections-callback-section />
   </main>
</template>
<script setup>
let path = [
   {
      name: "О нас",
      to: "/about",
   },
];
</script>
<style lang=""></style>
