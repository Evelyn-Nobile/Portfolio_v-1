<template>
   <div class="flex items-center justify-center mr-10 ml-10">
    <img src="../assets/brujita.png" alt="witch">
    <div>
      <span>FRONT-END DEVELOPER</span>
        <h2>Hi, there! I'm Evelyn Nobile</h2>
        <p class="text-justify w-1/2">I'm a junior front-end witch with basic knowledge of backend spells and database enchantments from Argentina.
          Currently, I'm seeking opportunities to brew my skills, work on what I love, and continue my magical journey of growth. 
          Forever a learner: I'm always in search of new spells to add to my repertoire.</p>
        <div>
           <button class="buttons"><ph-download-simple :size="32" />English resume</button>  
           <button class="buttons"><ph-github-logo :size="32" />Visit my Github</button>
        </div>
        <a href=""><ph-download-simple :size="32" />Descarga mi cv en español</a>
    </div>
   </div>
</template>

<script setup>
import { PhDownloadSimple, PhGithubLogo } from '@phosphor-icons/vue'
</script> 

<style scoped>
span, p, a {
  color: var(--text-color);
}
h2{
   color: var(--stress-color);
}
.buttons{
   background-color: var(--main-color);
   color: var(--text-color);
}

</style>