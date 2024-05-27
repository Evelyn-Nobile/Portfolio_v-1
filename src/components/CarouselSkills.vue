<template>
  <div class="carousel">
    <div class="carousel-container" :style="{ transform: 'translateX(' + slideOffset + ')' }">
      <div class="carousel-item" v-for="(icon, index) in iconComponents" :key="index">
        <div class="item-wrapper">
          <component :is="icon" class="carousel-svg" />
        </div>
      </div>
    </div>
    <button class="prev" @click="prevSlide">&lt;</button>
    <button class="next" @click="nextSlide">&gt;</button>
    <div class="pagination">
      <span
        v-for="(icon, index) in iconComponents"
        :key="index"
        @click="goToSlide(index)"
        :class="{ active: index === currentIndex }"
      ></span>
    </div>
  </div>
</template>

<script>
import { markRaw } from 'vue';

import HTML from '../SVG/HtmlSvg.vue';
import CSS from '../SVG/CssSvg.vue';
import JS from '../SVG/JsSvg.vue';
import React from '../SVG/ReactSvg.vue';
import Next from '../SVG/NextSvg.vue';
import Vue from '../SVG/VueSvg.vue';
import Nuxt from '../SVG/NuxtSvg.vue';
import Vite from '../SVG/ViteSvg.vue';
import Astro from '../SVG/AstroSvg.vue';
import Tailwind from '../SVG/TailwindSVG.vue';
import Bootstrap from '../SVG/BootSvg.vue';
import MUI from '../SVG/MaterialSvg.vue';
import Redux from '../SVG/ReduxSvg.vue';
import Node from '../SVG/NodeSvg.vue';
import Express from '../SVG/ExpressSvg.vue';
import PostgreSQL from '@/SVG/PostgreSQL';
import Sequelize from '../SVG/SequelizeSvg.vue';
import Axios from '../SVG/AxiosSvg.vue';
import Git from '../SVG/GitSvg.vue';
import GitHub from '../SVG/GithubSvg.vue';
import English from '../SVG/EnglishSvg.vue';
import Agile from  '../SVG/AgileSvg.vue';
import Vuex from '../SVG/VuexSvg.vue';
import Pinia from '../SVG/PiniaSvg.vue';

export default {
  components: {
    HTML: markRaw(HTML),
    CSS: markRaw(CSS),
    JS: markRaw(JS),
    React: markRaw(React),
    Next: markRaw(Next),
    Vue: markRaw(Vue),
    Nuxt: markRaw(Nuxt),
    Vite: markRaw(Vite),
    Astro: markRaw(Astro),
    Tailwind: markRaw(Tailwind),
    Bootstrap: markRaw(Bootstrap),
    MUI: markRaw(MUI),
    Redux: markRaw(Redux),
    Pinia: markRaw(Pinia),
    Vuex: markRaw(Vuex),
    Node: markRaw(Node),
    Express: markRaw(Express),
    PostgreSQL: markRaw(PostgreSQL),
    Sequelize: markRaw(Sequelize),
    Axios: markRaw(Axios),
    Git: markRaw(Git),
    GitHub: markRaw(GitHub),
    English: markRaw(English),
    Agile: markRaw(Agile)
  },
  data() {
    return {
      currentIndex: 0,
      iconComponents: [
        HTML, CSS, JS, React, Next, Vue, Nuxt, Vite, Astro, Tailwind, Bootstrap,
        MUI, Redux, Pinia, Vuex, Node, Express, PostgreSQL, Sequelize, Axios, Git,
         GitHub, English, Agile
      ],
      slideOffset: '0px'
    };
  },
  methods: {
    prevSlide() {
      if (this.currentIndex > 0) {
        this.currentIndex--;
        this.updateSlider();
      }
    },
    nextSlide() {
      if (this.currentIndex < this.iconComponents.length - 1) {
    this.currentIndex++;
  } else {
    this.currentIndex = 0; 
  }
  this.updateSlider();
    },
    goToSlide(index) {
      this.currentIndex = index;
      this.updateSlider();
    },
    updateSlider() {
      const slideWidth = 100; // Ancho de cada slide en porcentaje
      this.slideOffset = `-${slideWidth * this.currentIndex}%`;
    },
  },
};
</script>

<style scoped>
.carousel {
  position: relative;
  width: 100%;
  overflow: hidden;
  margin-top: 7rem;
}
.carousel-container {
  display: flex;
  transition: transform 0.3s ease-in-out;
}
.carousel-item {
  flex-shrink: 0;
  width: 100%;
}
.item-wrapper {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100%;
}
.carousel-svg {
  max-width: 100%;
  max-height: 100%;
}
.prev, .next {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  color: #333333;
  border: none;
  padding: 8px 16px;
  cursor: pointer;
  font-size: 35px;
}
.prev {
  left: 10px;
}
.next {
  right: 10px;
}
.pagination {
  display: flex;
  justify-content: center;
  margin-top: 50px;
}
.pagination span {
  cursor: pointer;
  margin: 0 5px;
  width: 8px;
  height: 8px;
  border-radius: 50%;
  background-color: #ccc;
  transition: background-color 0.3s ease;
}
.pagination span.active {
  background-color: #BD86E9;
}



@media screen and (max-width: 768px) {
  .pagination span {
  width: 12px; 
  height: 12px; 
  margin: 0 3px; 
}

  .pagination span {
    width: 8px; 
    height: 8px;
    margin: 0 2px; 
  }

  .carousel{
    margin-top: 3rem;
  }

  .prev, .next {
    font-size: 1.5rem;
   
  }

  .carousel-svg{
    width: 10rem;
    height: 6.5rem;
  }
}
</style>
