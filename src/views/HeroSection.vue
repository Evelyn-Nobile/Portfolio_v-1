<template>
   <section class="flex items-center justify-center flex-col mt-16 herocontainer" id="home">

      <div class="flex  items-center justify-center herocontent">
    <img src="https://res.cloudinary.com/dpxrcotbh/image/upload/v1716681834/evs4c59nvryntj02b5xf.webp" alt="logo">

    <div class=" p-6 herotextsContainer">
        <h1 class="text-4xl ">Living among cats, coffee and code</h1>
        <p class="text-justify mt-4 herotext">Hi!👋  I'm Evelyn, a junior front-end developer from Argentina,
         graduated from Henry's bootcamp and self-taught.
         Currently, I'm seeking opportunities to work in a company that allows me to showcase my skills, work on what I love, and continue growing. </p>
        
        <p> Forever a learner 🤓 </p>

        <div class="mt-8 flex  gap-6 justify-center items-center buttonsContainer">
         <button class="buttons flex gap-1 p-2.5 rounded-xl button-pink">
  <ph-download-simple :size="25" /><a href="https://drive.google.com/file/d/1minTIRSJ-r28tuAzx6fKR1Z-dRZcztg1/view?usp=sharing" target="_blank" rel="noopener noreferrer" class="linkDownload">English resume</a>
</button>


           <button class="buttons flex gap-1 p-2.5 rounded-xl button-lilac">
  <ph-github-logo :size="25" />
  <a href="https://github.com/Evelyn-Nobile" target="_blank" rel="noopener noreferrer" class="linkGithub">Visit my Github</a>
</button>          
        </div>

        <div class="mt-6 flex justify-center items-center ">
               <a href="https://drive.google.com/file/d/1Er6nxQq64GtrtvtbAwyrY5HmKiqu9uxT/view?usp=sharing" target="_blank" rel="noopener noreferrer" class="flex items-center gap-2 linkcv "><ph-download-simple :size="22" /> Descarga mi cv en español</a>
            </div>
       
    </div>
    
   </div>

   </section>
</template>

<script setup>
import { PhDownloadSimple, PhGithubLogo } from '@phosphor-icons/vue'
</script> 

<style scoped>

.herocontainer {
width: 95%;
max-width: 1800px
}


.herotextsContainer {
  width: 100%; 
}

p{
   width: 500px;
   max-width: 500px;
}

span, p, a {
  color: var(--text-color);
}

h1{
 font-family: "Style Script", cursive;
 font-weight: 800;
 color: var(--text-color);
 text-align: center;
 letter-spacing: 4px;
}

.linkcv{
   text-decoration: underline;
}



.buttons {
  width: 11rem;
  position: relative;
  transition: box-shadow 0.3s ease;
  border: 1px solid var(--text-color);

}

.buttons::after {
  content: '';
  position: absolute;
  bottom: -8px;
  right: -8px;
  width: 100%;
  height: 100%;
  border-radius: inherit;
  z-index: -1;
}

.button-pink::after {
  background-color: var(--pink-color);
}

.button-lilac::after {
  background-color: var(--lilac-color);
}



.buttons:active {
   transform: translate(2px, 2px);
}

.buttons:active::after {
  bottom: -6px;
  right: -6px;
}


/* responsive: */
@media screen and (max-width: 320px) {
   .herocontainer{
      width: 100%;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      margin-top: 2rem;
   }

   .herocontent{
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;

   }

   .herotextsContainer{
    width: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    padding: 0 1rem;
   

   }


h1{
font-size: 1.5rem;
text-align: center;
width: 100%;
max-width: 20rem;
margin: 0 1rem;
}

p{
width: 100%;
max-width: 25rem;
margin: 0 1rem;
margin-top: 2rem;

}



.buttonsContainer{
   display: flex;
   flex-direction: column;
}

.linkcv{
width: 100%;
font-size: 15px;
margin-top: 2rem;

   }

}


@media only screen and (min-width:321px) and (max-width:480px){
   .herocontainer{
      width: 100%;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      margin-top: 2rem;
   }

   .herocontent{
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;

   }

   .herotextsContainer{
    width: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    padding: 0 1rem;
   

   }


h1{
font-size: 1.5rem;
text-align: center;
width: 100%;
max-width: 20rem;
margin: 0 1rem;
}

p{
width: 100%;
max-width: 25rem;
margin: 0 1rem;
margin-top: 2rem;

}



.buttonsContainer{
   display: flex;
   flex-direction: column;
}

.linkcv{
width: 100%;
font-size: 15px;
margin-top: 2rem;

   }

}

@media (min-width: 481px) and (max-width: 759px) {
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

@media (min-width: 760px) and (max-width: 1023px) {
   .herocontainer{
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      margin-top: 2rem;  
      width: 80%; 
      
      
   }

  p{
      max-width: 350px;      
   }
   
  img{
      width: 50%;

  } 

 .linkcv{
   margin-right: 2rem;
   margin-top: 2rem;
 }

}



</style>