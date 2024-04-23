<template>
  <nav class="flex items-center justify-between flex-wrap p-6 mr-20 ml-20  ">
    <!-- <div class="flex items-center flex-shrink-0" :class="{ 'hidden': isMenuOpen }"> -->
      <div class="flex items-center flex-shrink-0">
      <img src="https://avatars.githubusercontent.com/u/102312214?v=4" alt="github-avatar" class="rounded-full w-10 h-10">
    </div>

    <div class="hidden lg:flex lg:items-center lg:w-auto navContainer">
      <div class="lg:flex-grow">
        <a href="#responsive-header" class="block mt-4 lg:inline-block lg:mt-0 mr-6 ">About me</a>
        <a href="#responsive-header" class="block mt-4 lg:inline-block lg:mt-0 mr-6 ">My Skills</a>
        <a href="#responsive-header" class="block mt-4 lg:inline-block lg:mt-0 mr-6 ">Projects</a>
        <a href="#responsive-header" class="block mt-4 lg:inline-block lg:mt-0 mr-6 ">Contact me</a>
      </div>
    </div>

    <div class="lg:hidden">
      <button id="boton" class="flex items-center px-3 py-2 border rounded bg-transparent toggle" @click="toggleMenu">
        <span v-if="!isMenuOpen">
          <svg class="fill-current h-3 w-3" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
            <title>Menú</title>
            <path d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z" />
          </svg>
        </span>
      </button>
      <transition name="menu-bubble">
        <div v-if="isMenuOpen" class="lg:hidden absolute top-0 right-0 h-2/3 w-3/4 rounded-l-full flex flex-col justify-center items-center bubbleEffect">
          <a @click="closeMenu" href="#responsive-header" class=" bubbleText mb-3">About me</a>
          <a @click="closeMenu" href="#responsive-header" class="bubbleText mb-3">My Skills</a>
          <a @click="closeMenu" href="#responsive-header" class=" bubbleText mb-3">Projects</a>
          <a @click="closeMenu" href="#responsive-header" class=" bubbleText mb-3">Contact</a>
          <span @click="closeMenu" class="text-lg menuClose">x</span>
        </div>
      </transition>
    </div>
  </nav>
</template>

<script setup>
import { ref } from 'vue';

const isMenuOpen = ref(false);

function toggleMenu() {
  isMenuOpen.value = !isMenuOpen.value;
}

function closeMenu() {
  isMenuOpen.value = false;
}
</script>

<style scoped>

@media screen and (min-width: 1024px) {
nav {
  position: sticky;
  z-index: 1;
  top: 0;
box-shadow: 0px 2px 2px rgba(136, 43, 243, 0.2);
  backdrop-filter: blur(10px);
  border-radius: 20px;
}
}
.navContainer a {
  color: var(--text-color);
  transition: color 0.3s ease, border-bottom-color 0.3s ease; 
  border-bottom: 2px solid transparent; 
  text-decoration: none;
}

.navContainer a:hover {
  color: var(--stress-color); 
  border-bottom-color: var(--stress-color); 
}


/* Estilos para el botón de hamburguesa */
#boton {
  display: block;
  border: none; 
  background-color: transparent; 
}

svg {
  cursor: pointer;
  height: 24px;
  width: 24px;
}

.menuClose, .toggle{
  color: var(--text-color);
  cursor: pointer;
}
.menu-bubble-enter-active {
  animation: menu-bubble-enter 0.3s ease-out;
}

.menu-bubble-leave-active {
  animation: menu-bubble-leave 0.3s ease-out;
}
.bubbleEffect {
  background-color: var(--main-color); 
}
.bubbleText {
  font-size: 18px; 
  color: var(--text-color);
}

@keyframes menu-bubble-enter {
  from {
    opacity: 0;
    transform: scale(0.5);
  }
  to {
    opacity: 1;
    transform: scale(1);
  }
}

@keyframes menu-bubble-leave {
  from {
    opacity: 1;
    transform: scale(1);
  }
  to {
    opacity: 0;
    transform: scale(0.5);
  }
}
</style>
