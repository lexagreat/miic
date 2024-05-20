<template>
   <main class="main">
      <ui-app-breadcrumbs :path="[{}]" />
      <sections-home-hero />
      <sections-nav-section />
      <sections-home-experience
         class="scroll-section"
         data-scroll="experience"
      />
      <sections-services-section
         class="scroll-section"
         data-scroll="services"
      />
      <sections-team-section class="scroll-section" data-scroll="team" />
      <sections-cases-section class="scroll-section" data-scroll="cases" />
      <sections-partners-section
         class="scroll-section"
         data-scroll="partners"
      />
      <sections-sale-banner />
      <sections-faq-section />
      <sections-callback-section />
   </main>
</template>
<script setup></script>
<style lang=""></style>
