<template>
   <section class="section brief-section">
      <div class="container">
         <div class="brief-section__wrapper">
            <div class="brief-section__header">
               <h2 class="brief-section__title">
                  Компания МИИК — Ваш надежный IT-партнер
               </h2>
               <p class="brief-section__text">
                  Заполните заявку, наш менеджер свяжется с Вами в течение 15
                  минут!
               </p>
            </div>
            <div class="brief-section__content">
               <div class="brief-section__form">
                  <ul class="brief-section__list">
                     <li>
                        <form-text-input
                           id="name"
                           placeholder="Имя"
                           v-model="name"
                        />
                     </li>
                     <li>
                        <form-text-input
                           id="company"
                           placeholder="Название компании"
                           v-model="company"
                        />
                     </li>
                     <li>
                        <form-text-input
                           id="email"
                           placeholder="Email"
                           v-model="email"
                           isEmail
                        />
                     </li>
                     <li>
                        <form-text-input
                           id="phone"
                           placeholder="Номер телефона"
                           v-model="phone"
                           :isPhone="true"
                        />
                     </li>
                     <button class="brief-section__send btn yellow">
                        Отправить
                     </button>
                     <p class="brief-section__remind">
                        Нажимая на кнопку, вы даете
                        <nuxt-link to="/">согласие</nuxt-link> на обработку
                        <nuxt-link to="/">персональных данных</nuxt-link>
                     </p>
                  </ul>
               </div>
               <div class="brief-section__info">
                  <h4 class="brief-section__subtitle">Наши контакты</h4>
                  <div class="brief-section__contacts">
                     <ul>
                        <li>
                           <nuxt-link to="tel:+7 (999) 333-44-55"
                              >+7 (999) 333-44-55</nuxt-link
                           >
                        </li>
                        <li>
                           <nuxt-link to="mailto:Miic.pro@help.com"
                              >Miic.pro@help.com</nuxt-link
                           >
                        </li>
                     </ul>
                     <ul>
                        <li>
                           <nuxt-link to="https://web.telegram.org/a/"
                              >Telegram</nuxt-link
                           >
                        </li>
                        <li>
                           <nuxt-link to="https://www.whatsapp.com/?lang=ru_RU"
                              >WhatsApp</nuxt-link
                           >
                        </li>
                     </ul>
                  </div>
               </div>
            </div>
         </div>
      </div>
   </section>
</template>
<script setup>
let name = ref("");
let company = ref("");
let email = ref("");
let phone = ref("");
</script>
