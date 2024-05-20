<template lang="">
   <section class="home-navigation">
      <div class="container">
         <ul class="home-navigation__list">
            <li>
               <nuxt-link
                  data-scroll="experience"
                  class="home-navigation__link btn active"
                  >Опыт работы</nuxt-link
               >
            </li>
            <li>
               <nuxt-link
                  data-scroll="services"
                  class="home-navigation__link btn"
                  >Услуги</nuxt-link
               >
            </li>
            <li>
               <nuxt-link data-scroll="team" class="home-navigation__link btn"
                  >Специалисты IT</nuxt-link
               >
            </li>
            <li>
               <nuxt-link data-scroll="cases" class="home-navigation__link btn"
                  >Кейсы</nuxt-link
               >
            </li>
            <li>
               <nuxt-link
                  data-scroll="partners"
                  class="home-navigation__link btn"
                  >Партнеры</nuxt-link
               >
            </li>
         </ul>
      </div>
   </section>
</template>
<script setup>
let headerHeight, sticky, navbar;
function makeNavSticky() {
   if (window.pageYOffset + 24 + headerHeight >= sticky) {
      navbar.classList.add("sticky");
   } else {
      navbar.classList.remove("sticky");
   }
}

function mainPageNavigation() {
   const links = document.querySelectorAll(".home-navigation__link");
   const sections = document.querySelectorAll(".scroll-section");
   if (!links.length) {
      return;
   }
   links.forEach((link) => {
      link.addEventListener("click", () => {
         let id = link.getAttribute("data-scroll");
         // link.classList.add("active");
         sections.forEach((section) => {
            if (section.getAttribute("data-scroll") === id) {
               console.log(section);
               window.scrollBy({
                  top: section.getBoundingClientRect().top - headerHeight,
                  behavior: "smooth",
               });
            }
         });
      });
   });

   const callback = (entries, observer) => {
      entries.forEach((entry) => {
         if (!entry.isIntersecting && entry.boundingClientRect.top < 0) {
            let section = entry.target?.nextElementSibling;
            if (!section || !section.getAttribute("data-scroll")) {
               return;
            }
            let id = section.getAttribute("data-scroll");
            links.forEach((link) => {
               link.classList.remove("active");
               if (link.getAttribute("data-scroll") === id) {
                  link.classList.add("active");
               }
            });
         } else {
            if (entry.boundingClientRect.top < 0) {
               let section = entry.target;
               if (!section || !section.getAttribute("data-scroll")) {
                  return;
               }
               let id = section.getAttribute("data-scroll");
               links.forEach((link) => {
                  link.classList.remove("active");
                  if (link.getAttribute("data-scroll") === id) {
                     link.classList.add("active");
                  }
               });
            }
         }
      });
   };

   const options = {
      // root: по умолчанию window, но можно задать любой элемент-контейнер
      rootMargin: "0px 0px 75px 0px",
      threshold: 0,
   };

   const observer = new IntersectionObserver(callback, options);

   sections.forEach((section) => observer.observe(section));
}

onMounted(() => {
   navbar = document.querySelector(".home-navigation");
   sticky = navbar.offsetTop;
   headerHeight = document
      .querySelector(".header")
      .getBoundingClientRect().height;
   window.addEventListener("scroll", makeNavSticky);
   makeNavSticky();
   mainPageNavigation();
});
onBeforeUnmount(() => {
   window.removeEventListener("scroll", makeNavSticky);
});
</script>
<style lang=""></style>
