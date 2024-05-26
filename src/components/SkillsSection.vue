<template>
    <div class="skillscontainer mt-6">
        <div class="flex  flex-col  justify-items-start  my-4">
            <h1 class="text-3xl mr-2">My Skills...</h1>
            <span class="text-lg mt-4">Technologies and tools learned so far:</span>
            
        </div>
        </div>
        <CarouselSkills/>
       
    
</template>

<script setup>
import CarouselSkills from './CarouselSkills.vue'


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
    
    top: 0;
    
}
</style>
