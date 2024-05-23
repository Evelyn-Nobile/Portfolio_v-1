<template>
    <div class="projectscontainer mt-6">

        <div class="flex  flex-col  justify-items-start  my-4">
            <h1 class="text-3xl mr-2">My Projects</h1>            
        </div>
        <div class="grid grid-cols-3 gap-6 mt-12">
            <div v-for="project in projects" :key="project.name" class="project-card overflow-hidden shadow-md w-96 h-full">
                <div class="image-container relative w-full h-52 ">
                    <img :src="project.img" :alt="project.name" class="project-image  w-full h-full object-cover" />
                    <div class="overlay">
                        <p>{{ project.description }}</p>
                    </div>
                </div>
                <h2 class="project-title">{{ project.name }}</h2>
                <div class="mb-6 flex flex-wrap justify-center align-center gap-4 project-tags">
                    <component v-for="tag in project.tags" :is="getIconComponent(tag)" :key="tag" class="w-17 h-14"></component>
                </div>
                <div class="project-links mb-4 flex justify-center align-center gap-6">
                    <a :href="project.repository" target="_blank">Repository</a>
                    <a v-if="project.link" :href="project.link" target="_blank">Live Demo</a>
                </div>
            </div>
        </div>
    </div>




      

       
    
</template>

<script setup>
import { ref } from 'vue';
import { projects as projectsData } from './../projects.js';
import NextIcon from '../SVG/NextSvg.vue';
import TailwindIcon from '../SVG/TailwindSVG.vue';
import BootstrapIcon from '../SVG/BootSvg.vue';
import ReactIcon from '../SVG/ReactSvg.vue';
import ReduxIcon from '../SVG/ReduxSvg.vue';
import VueIcon from '../SVG/VueSvg.vue';
import ViteIcon from '../SVG/ViteSvg.vue';
import NodeIcon from '../SVG/NodeSvg.vue';
import ExpressIcon from '../SVG/ExpressSvg.vue';
import PostgreSQLIcon from '../SVG/PostgreSQL.vue';
import SequelizeIcon from '../SVG/SequelizeSvg.vue';
import HTMLIcon from '../SVG/HtmlSvg.vue';
import CSSIcon from '../SVG/CssSvg.vue';
import JSIcon from '../SVG/JsSvg.vue';



const projects = ref(projectsData);

const getIconComponent = (tag) => {
    const icons = {
        "NextJs": NextIcon,
        "Tailwind": TailwindIcon,
        "Bootstrap": BootstrapIcon,
        "React": ReactIcon,
        "Vue": VueIcon,
        "Vite": ViteIcon,
        "Node": NodeIcon,
        "Express": ExpressIcon,
        "PostgreSQL": PostgreSQLIcon,
        "Sequelize": SequelizeIcon,
        "Redux": ReduxIcon,
        "HTML": HTMLIcon,
        "CSS": CSSIcon,
        "JS": JSIcon
        
    };

    return icons[tag] || null;
};
</script>

<style scoped>
.projectscontainer {
    margin-left: 7rem; 
    padding-left: 0; 
    margin-top: 7rem;
}


h1 {
    color: var(--stress-color);
    margin-left: 0; 
}

.project-card {
    border: 4px solid var(--stress-color);
    border-radius: 15px;
}


.overlay {
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: rgba(0, 0, 0, 0.7);
    color: white;
    opacity: 0;
    display: flex;
    align-items: center;
    justify-content: center;
    text-align: center;
    padding: 1rem;
    transition: opacity 0.3s;
}

.image-container:hover .overlay {
    opacity: 1;
}

.project-title {
    margin: 1rem;
    font-size: 1.2rem;
    font-weight: bold;
    text-align: center;
    color: var(--stress-color);
}


.project-links {
    color: var(--text-color);
}

</style>
