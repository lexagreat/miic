<template lang="">
   <section class="section cases-section">
      <div class="container">
         <div class="section__wrapper cases-section__wrapper">
            <h2 class="cases-section__title h2">Наши кейсы</h2>
            <div class="cases-section__content">
               <ul class="cases-section__filters">
                  <li v-for="(item, index) in filters" :key="item">
                     <input
                        type="radio"
                        v-model="filter"
                        :id="'filter' + index"
                        :value="'value' + index"
                        name="filter"
                     />
                     <label :for="'filter' + index" class="btn">{{
                        item.name
                     }}</label>
                  </li>
               </ul>
               <ul class="cases-section__list">
                  <li v-for="item in 3" :key="item">
                     <case-card />
                  </li>
               </ul>
            </div>
            <div class="cases-section__footer">
               <button class="cases-section__pagination btn">
                  смотреть еще
               </button>
            </div>
         </div>
      </div>
   </section>
</template>
<script setup>
const filter = defineModel({ default: "value0" });
const filters = [
   {
      name: " Маркет плейсы",
   },
   {
      name: "Сайты",
   },
   {
      name: "Аудиты",
   },
   {
      name: "СКУД",
   },
   {
      name: "Видеонаблюдение",
   },
   {
      name: "ИТ-аутсорсинг",
   },
];
</script>
<style lang=""></style>
