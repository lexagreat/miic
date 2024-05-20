<template lang="">
   <header class="header">
      <div class="container">
         <div class="header__wrapper">
            <div class="header__logo">
               <nuxt-link to="/">
                  <img src="@/assets/img/icons/logo.svg" alt="" />
               </nuxt-link>
            </div>
            <div class="header__menu" :class="{ active: isMenuOpen }">
               <ul class="header__list">
                  <li :class="{ active: isSubmenuOpen && windowWidth <= 992 }">
                     <button
                        class="header__link header__sublink"
                        @click.prevent="openSubmenu"
                     >
                        <span>Услуги</span>
                        <svg
                           width="8"
                           height="6"
                           viewBox="0 0 8 6"
                           fill="none"
                           xmlns="http://www.w3.org/2000/svg"
                        >
                           <path
                              d="M0.666667 4.66663L4 1.33329L7.33333 4.66663"
                              stroke="#6A6A6A"
                              stroke-linecap="round"
                              stroke-linejoin="round"
                           />
                        </svg>
                     </button>
                     <div
                        class="header__spoiler"
                        :class="{ collapse: windowWidth <= 992 }"
                        ref="spoiler"
                     >
                        <ul>
                           <li>
                              <nuxt-link to="/">
                                 Системы видеонаблюдения под ключ
                              </nuxt-link>
                           </li>
                           <li>
                              <nuxt-link to="/">
                                 Системы контроля и управления доступом (СКУД)
                              </nuxt-link>
                           </li>
                           <li>
                              <nuxt-link to="/">
                                 Услуги ИТ-аутсорсинга для бизнеса
                              </nuxt-link>
                           </li>
                           <li>
                              <nuxt-link to="/"> Поддержка 1С </nuxt-link>
                           </li>
                           <li>
                              <nuxt-link to="/">
                                 Удаленные рабочие места
                              </nuxt-link>
                           </li>
                           <li>
                              <nuxt-link to="/">
                                 Комплекс базовых IT-услуг для бизнеса
                              </nuxt-link>
                           </li>
                           <li>
                              <nuxt-link to="/">
                                 Проведение аудита ИТ-инфраструктуры предприятия
                              </nuxt-link>
                           </li>
                           <li>
                              <nuxt-link to="/">
                                 Разработка и внедрение ИТ-инфраструктуры с нуля
                              </nuxt-link>
                           </li>
                           <li>
                              <nuxt-link to="/">
                                 Терминальные сервера
                              </nuxt-link>
                           </li>
                        </ul>
                     </div>
                  </li>
                  <li>
                     <nuxt-link to="/" class="header__link"
                        ><span>Цены</span></nuxt-link
                     >
                  </li>
                  <li>
                     <nuxt-link to="/about" class="header__link"
                        ><span>О нас</span></nuxt-link
                     >
                  </li>
               </ul>
            </div>
            <button class="header__order btn yellow">Заказать звонок</button>
            <button
               class="header__burger"
               @click="headerWork"
               :class="{ active: isMenuOpen }"
            >
               <span></span>
            </button>
         </div>
      </div>
   </header>
</template>
<script setup>
import { slideToggle } from "#imports";
import { ref, onMounted, onUnmounted } from "vue";
let isSubmenuOpen = ref(false);
let isMenuOpen = ref(false);
let spoiler = ref(null);

let windowWidth = ref(0);

function headerWork() {
   isMenuOpen.value = !isMenuOpen.value;
}

function handleResize() {
   windowWidth.value = window?.innerWidth;
}
function openSubmenu() {
   if (window.innerWidth > 992) {
      return;
   }
   isSubmenuOpen.value = !isSubmenuOpen.value;
   slideToggle(spoiler.value);
}

onMounted(() => {
   handleResize();
   window.addEventListener("resize", handleResize);
});
onUnmounted(() => {
   window.removeEventListener("resize", handleResize);
});
</script>
<style lang=""></style>
