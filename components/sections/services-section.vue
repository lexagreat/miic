<template lang="">
   <section class="services-section section">
      <div class="container">
         <div class="services-section__wrapper">
            <h2 class="services-section__title h2">
               Каталог услуг IT от компании МИИК
            </h2>
            <ul class="services-section__list">
               <li v-for="item in 9">
                  <nuxt-link class="services-card">
                     <div class="services-card__icon">
                        <img
                           src="@/assets/img/icons/services-icon.svg"
                           alt=""
                        />
                     </div>
                     <div class="services-card__main">
                        <div class="services-card__title">
                           Услуги ИТ-аутсорсинга для бизнеса
                        </div>
                        <button class="services-card__btn">подробнее</button>
                     </div>
                  </nuxt-link>
               </li>
            </ul>
         </div>
      </div>
   </section>
</template>
<script>
export default {};
</script>
<style lang=""></style>
