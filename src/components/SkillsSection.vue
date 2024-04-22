<template>
    <div class="skillscontainer mt-6">
        <div class="flex items-center my-4">
            <h1 class="text-3xl mr-2">My Skills</h1>
            <img src="../assets/pocion.png" alt="potion" class="potionimg">
        </div>
        </div>
        <!-- <span>Tecnical skills learned so far:</span> -->
        <div class="flex flex-col gap-6 mt-12">
        <div  class="flex justify-evenly items-center ">       
        <HTML/>
        <CSS/>
        <JS/>
        <React/>
        <Next/>
        </div>

        <div  class="flex justify-evenly items-center "> 
        <Vue/>
        <Nuxt/>
        <Vite/>
        <Astro/>
        <Tailwind/>
        </div>

        <div  class="flex justify-evenly items-center"> 
        <Bootstrap/>
        <MUI/>
        <Redux/>
        <Node/>
        <Express/>
        </div>

        <div  class="flex justify-evenly items-center"> 
        <PostgreSQL/>
        <Sequelize/>
        <Axios/>
        <Git/>
        <GitHub/>
        </div>

    </div>

   
    
    <div>
        <span class="text-lg flex justify-center items-center mt-12">To be continued...</span>
        
    </div>
</template>

<script setup>
import HTML from '../SVG/HtmlSvg.vue'
import CSS from '../SVG/CssSvg.vue'
import JS from '../SVG/JsSvg.vue'
import React from '../SVG/ReactSvg.vue'
import Next from '../SVG/NextSvg.vue'
import Vue from '../SVG/VueSvg.vue'
import Nuxt from '../SVG/NuxtSvg.vue'
import Vite from '../SVG/ViteSvg.vue'
import Astro from '../SVG/AstroSvg.vue'
import Tailwind from '../SVG/TailwindSVG.vue'
import Bootstrap from '../SVG/BootSvg.vue' 
import MUI from '../SVG/MaterialSvg.vue'
import Redux from '../SVG/ReduxSvg.vue'
import Node from '../SVG/NodeSvg.vue'
import Express from '../SVG/ExpressSvg.vue'
import PostgreSQL from '@/SVG/PostgreSQL'
import Sequelize from '../SVG/SequelizeSvg.vue'
import Axios from '../SVG/AxiosSvg.vue'
import Git from '../SVG/GitSvg.vue'
import GitHub from '../SVG/GithubSvg.vue'

</script>

<style scoped>
.skillscontainer {
    margin-left: 7rem; 
    padding-left: 0; 
    margin-top: 5rem;
}

.potionimg {
    width: 65px;
    height: 90px;
}

h1 {
    color: var(--stress-color);
    margin-left: 0; 
}


img {
    margin-left: 0;
}
span{
    color: var(--text-color);
    
}
</style>
