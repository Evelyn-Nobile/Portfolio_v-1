<template>
    <section class="skillscontainer mt-6" id="skills">
        <div class="flex  flex-col  justify-items-start  my-4 textsContainer ">
            <h1 class="text-3xl mr-2">My Skills...</h1>
            <span class="text-lg mt-4">Technologies and tools learned so far:</span>
            
        </div>
        </section>

       

        <div class="grid grid-cols-5 mt-8 gap-8 SVGContainer">
         
          <HtmlSvg/>
          <CssSvg/>
          <JsSvg/>
          <ReactSvg/>
          <NextSvg/>
          <ReduxSvg/>
          <VueSvg/>
          <ViteSvg/>
          <DartSvg/>
          <FlutterSvg/>
          <TailwindSvg/>
          <BootSvg/>          
          <MUISvg/>
          <NodeSvg/>
          <ExpressSvg/>
          <PostgreSQLSvg/>
          <SequelizeSvg/>         
          <AxiosSvg/>
          <GitSvg/>
          <GithubSvg/>
          <EnglishSvg/>
          <AgileSvg/>
        </div>

       
    
</template>

<script setup>
import AgileSvg from '@/SVG/AgileSvg.vue';

import BootSvg from '@/SVG/BootSvg.vue';
import CssSvg from '@/SVG/CssSvg.vue';
import HtmlSvg from '@/SVG/HtmlSvg.vue';
import JsSvg from '@/SVG/JsSvg.vue';
import ReactSvg from '@/SVG/ReactSvg.vue';
import ReduxSvg from '@/SVG/ReduxSvg.vue';
import TailwindSvg from '@/SVG/TailwindSVG.vue';
import VueSvg from '@/SVG/VueSvg.vue';
import ViteSvg from '@/SVG/ViteSvg.vue';
import NodeSvg from '@/SVG/NodeSvg.vue';
import ExpressSvg from '@/SVG/ExpressSvg.vue';
import PostgreSQLSvg from '@/SVG/PostgreSQL.vue';
import SequelizeSvg from '@/SVG/SequelizeSvg.vue';
import NextSvg from '@/SVG/NextSvg.vue';
import AxiosSvg from '@/SVG/AxiosSvg.vue';
import EnglishSvg from '@/SVG/EnglishSvg.vue';
import GitSvg from '@/SVG/GitSvg.vue';
import GithubSvg from '@/SVG/GithubSvg.vue';
import MUISvg from '@/SVG/MaterialSvg.vue';
import FlutterSvg from '@/SVG/FlutterSvg.vue';
import DartSvg from '@/SVG/DartSvg.vue';



</script>

<style scoped>
.skillscontainer {
  max-width: 1800px; 
  margin: 7rem auto 0; 
  padding: 0 2rem; 
}


h1 {
  text-align: left;
  font-family: 'Style Script', cursive;
  font-weight: 800;
  font-size: 2rem;
  letter-spacing: 4px;
  color: var(--text-color);
}

span{
    color: var(--text-color);
    margin-top: 0 ;
    
}

/* responsive: */
@media screen and (max-width: 320px) {
    .skillscontainer {
    margin-left: 0;
    padding-left: 1rem;
    margin-top: 5rem;
  }

  .textsContainer {
    align-items: center; 
    justify-content: center; 
  }

  h1 {
    font-size: 1.5rem;
    width: 100%;
    max-width: 20rem;
    text-align: center;
  }

  span {
    font-size: 0.8rem;
    width: 100%;
    max-width: 20rem;
    margin-top: 0;
    text-align: center;
  }
    
.SVGContainer {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  margin-top: 2rem;
}
}

@media only screen and (min-width:321px) and (max-width:480px){
  .skillscontainer {
    margin-left: 0;
    padding-left: 1rem;
    margin-top: 5rem;
  }
  .SVGContainer {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  margin-top: 2rem;
}
  .textsContainer {
    align-items: center; 
    justify-content: center; 
  }

  h1 {
    font-size: 1.5rem;
    width: 100%;
    max-width: 20rem;
    text-align: center;
  }

  span {
    font-size: 0.8rem;
    width: 100%;
    max-width: 20rem;
    margin-top: 0;
    text-align: center;
  }
}

@media (min-width: 481px) and (max-width: 759px) {
  .skillscontainer {
    margin-left: 0;
    padding-left: 1rem;
    margin-top: 5rem;
  }

  .textsContainer {
    align-items: center; 
    justify-content: center; 
  }

  h1 {
    font-size: 2rem;
    width: 100%;
    max-width: 20rem;
    text-align: center;
  }

  span {
    font-size: 1rem;
    width: 100%;
    max-width: 20rem;
    margin-top: 0;
    text-align: center;
  } 

.SVGContainer {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  margin-top: 2rem;
}
}

@media (min-width: 760px) and (max-width: 1024px) {
   
  .skillscontainer {
    margin-left: 0;
    padding-left: 1rem;
    margin-top: 5rem;

  }

  .textsContainer {
    align-items: center; 
    justify-content: center; 
  }

  h1 {
    font-size: 2rem;
    width: 100%;
    max-width: 20rem;
    text-align: center;
  }

  span {
    font-size: 1rem;
    width: 100%;
    max-width: 20rem;
    margin-top: 0;
    text-align: center;
  }
}


</style>
