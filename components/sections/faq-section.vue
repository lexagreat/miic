<template lang="">
   <section class="section faq-section">
      <div class="container">
         <div class="faq-section__wrapper section__wrapper">
            <h2 class="faq-section__title h2">Часто задаваемые вопросы</h2>
            <ul class="faq-section__list">
               <li
                  class="faq-section__item faq-item"
                  v-for="item in 4"
                  :key="item"
               >
                  <div class="faq-item__header">
                     <div class="faq-item__title">
                        Как узнать цены на ИТ-услуги для бизнеса?
                     </div>
                     <div class="faq-item__icon">
                        <img src="@/assets/img/icons/faq-icon.svg" alt="" />
                     </div>
                  </div>
                  <div class="faq-item__content collapse">
                     <p>
                        Как узнать цены на ИТ-услуги для бизнеса? Как узнать
                        цены на ИТ-услуги для бизнеса? Как узнать цены на
                        ИТ-услуги для бизнеса? Как узнать цены на ИТ-услуги для
                        бизнеса?
                     </p>
                  </div>
               </li>
            </ul>
         </div>
      </div>
   </section>
</template>
<script setup>
import accordion from "~/utils/accordion";
import { onMounted } from "vue";

onMounted(() => {
   accordion(".faq-item__header", ".faq-item__content");
});
</script>
<style lang=""></style>
