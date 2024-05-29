<template>
    <section class="skillscontainer mt-6" id="skills">
        <div class="flex  flex-col  justify-items-start  my-4 textsContainer ">
            <h1 class="text-3xl mr-2">My Skills...</h1>
            <span class="text-lg mt-4">Technologies and tools learned so far:</span>
            
        </div>
        </section>
        <CarouselSkills/>
       
    
</template>

<script setup>
import CarouselSkills from '../components/CarouselSkills.vue';


</script>

<style scoped>
.skillscontainer {
    margin-left: 7rem; 
    padding-left: 0; 
    margin-top: 7rem;
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
    

}


@media only screen and (min-width:321px) and (max-width:480px){
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
