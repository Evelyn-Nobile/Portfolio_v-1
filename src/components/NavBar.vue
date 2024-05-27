<template>
  <nav class="flex items-center  p-6 w-full">
  

    <!-- Navigation links for larger screens -->
    <div class="hidden lg:flex  lg:w-auto navContainer">
      <div class="lg:flex-grow flex justify-end items-center ">
        <a href="#home" class="block mt-4 lg:inline-block lg:mt-0">Home</a>
        <a href="#skills" class="block mt-4 lg:inline-block lg:mt-0">My Skills</a>
        <a href="#learning" class="block mt-4 lg:inline-block lg:mt-0">Learning</a>
        <a href="#projects" class="block mt-4 lg:inline-block lg:mt-0">Projects</a>
        <a href="#contact" class="block mt-4 lg:inline-block lg:mt-0">Contact me</a>
      </div>
    </div>

    <!-- Menu toggle button for smaller screens -->
    <div class="lg:hidden flex items-center ml-auto">
      <button id="boton" class="flex items-center px-3 py-2 border rounded bg-transparent toggle" @click="toggleMenu">
        <span v-if="!isMenuOpen">
          <svg class="fill-current h-5 w-5" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
            <path d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z" />
          </svg>
        </span>
      </button>
    </div>

    <!-- Bubble menu for smaller screens -->
    <transition name="menu-bubble">
      <div v-if="isMenuOpen" class="lg:hidden absolute top-0 right-0 h-1/2 w-1/2 rounded-l-full flex flex-col justify-center items-center bubbleEffect">
        <span @click="closeMenu" class="text-lg menuClose">x</span>
        <a @click="closeMenu" href="#home" class="bubbleText mb-3">Home</a>
        <a @click="closeMenu" href="#skills" class="bubbleText mb-3">My Skills</a>
        <a @click="closeMenu" href="#learning" class="bubbleText mb-3">Learning</a>
        <a @click="closeMenu" href="#projects" class="bubbleText mb-3">Projects</a>
        <a @click="closeMenu" href="#contact" class="bubbleText mb-3">Contact</a>
      
      </div>
    </transition>
  </nav>
 
</template>


<script setup>
import { ref} from 'vue';

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
    position: fixed;
    z-index: 1000;
    top: 0;
    width: 100%;
    box-shadow: 0px 6px 8px rgba(0, 0, 0, 0.2);
    background-color: #ecdfeb;
   

  }


  .navContainer {
    flex-grow: 1;
    display: flex;
    justify-content: flex-start;
    align-items: center;

  }
}

.navContainer a {
  color: var(--text-color);
  transition: color 0.3s ease, border-bottom-color 0.3s ease;
  border-bottom: 2px solid transparent;
  text-decoration: none;
  margin-right: 20px;
}

.navContainer a:hover {
  color: var(--text-color);
  border-bottom-color: var(--text-color);
}


/* Estilos para el botón de hamburguesa */


#boton {
  display: block;
  border: none; 
  background-color: transparent;
  cursor: pointer; 

}

svg {
  cursor: pointer;
  height: 24px;
  width: 24px;
display: flex;

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
  background-color: var(--lilac-color); 
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
