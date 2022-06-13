<template>
   <header class="header">
      <div class="header__container">
         <nav class="menu">
            <router-link to="/" >
               <img class="menu__logo" src="https://www.vectorlogo.zone/logos/vuejs/vuejs-icon.svg" alt="Vue JS logo">
            </router-link>
            <ul class="menu__list">
               <li class="menu__item" v-for="link in links" :key="link.alias">
                  <routerLink class="menu__link" :to="link.url">{{link.title}}</routerLink>
               </li>
            </ul>
         </nav>
      </div>
   </header>
</template>

<script>
import {links} from '@/_config';

export default {
  data() {
      return {
         links: links,   
      };
  },
};
</script>