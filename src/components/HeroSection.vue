<template>
   <div class="flex items-center justify-center  flex-col mt-16 herocontainer ">
      <div class="w-1/2 flex  items-center justify-center herocontent">
    <img src="../assets/WhatsApp Image 2024-04-23 at 20.56.41 (1).jpeg" alt="witch">
    <div class=" p-6 herotextsContainer">
      <span>FRONT-END DEVELOPER</span>
        <h1 class="text-4xl ">Hi, there! I'm Evelyn Nobile</h1>
        <p class="text-justify mt-4 herotext">I'm a junior front-end developer from Argentina,
         graduated from Henry's bootcamp and self-taught.
         Currently, I'm seeking opportunities to work in a company that allows me to showcase my skills, work on what I love, and continue growing. Forever a learner 🤓 </p>
        <div class="mt-8 flex gap-6 justify-center items-center">
         <button class="buttons flex gap-1 p-2.5 rounded-xl">
  <ph-download-simple :size="25" /><a href="https://drive.google.com/file/d/1CR-z6w8la1tObe3mguXMIiGgNGcTW4N3/view?usp=sharing" target="_blank" rel="noopener noreferrer" class="linkDownload">English resume</a>
</button>


           <button class="buttons flex gap-1 p-2.5 rounded-xl">
  <ph-github-logo :size="25" />
  <a href="https://github.com/Evelyn-Nobile" target="_blank" rel="noopener noreferrer" class="linkGithub">Visit my Github</a>
</button>
          
        </div>
        <div class="mt-6 flex justify-center items-center ">
               <a href="https://drive.google.com/file/d/1GF1M_mPVsN1MNynPruPLzJQUivBq4m5A/view?usp=sharing" target="_blank" rel="noopener noreferrer" class="flex items-center gap-2 linkcv "><ph-download-simple :size="22" /> Descarga mi cv en español</a>
            </div>
       
    </div>
    
   </div>

</div>
</template>

<script setup>
import { PhDownloadSimple, PhGithubLogo } from '@phosphor-icons/vue'
</script> 

<style scoped>

.herocontainer {
width: 95%;
}
.herotextsContainer {
  width: 100%; 
}
p{
   width: 500px;
}
span, p, a {
  color: var(--text-color);
}

h1{
   color: var(--stress-color);
}

.linkcv{
   text-decoration: underline;
}
a:hover{
  color: #e0b0ff;
  
}
.buttons{
   background-color: var(--main-color);
   color: var(--text-color);
   width: 11rem;
}

.buttons:hover {
  background-color: #7f00b2;
}

img{
   width: 350px;
   height: 350px;
   border-radius: 10%;
}

/* responsive: */
@media (min-width: 760px) and (max-width: 1023px) {
   .herocontainer{
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      margin-top: 2rem;
      
   }

  p{
      max-width: 350px;
   }
}

@media screen and (max-width: 759px) {
   .herotextsContainer{
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
   }

p, h1, span,a{
 width: 350px;
}


   .herocontent{
      display: flex;
      flex-direction: column;
   }

   .buttons{
      width: 160px;
      text-align: center;
      
   }

 a{
   display: flex;
   justify-content: center;
   align-items: center;
 }
}

</style>