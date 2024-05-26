<template>
    <div class="currentlyContainer mt-6">
        <h1 class="text-3xl mr-2" >Currently Learning...</h1>

        <div class="mt-12 flex flex-col items-start gap-1 barContainer">
            <h3 class="text-xl ">Python Basics - Codo a Codo </h3>
            <p class="text-justify  text-sm">198-hour course whose syllabus is: Review of HTML, CSS and JavaScript. SQL, MySQL, Scrum, Python, OOP and Flask.</p>

<div class="w-1/2 bg-gray-200 rounded-full dark:bg-gray-700 overflowBar ">
  <div class="progress-bar text-xs font-medium text-purple-100 text-center p-0.5 leading-none rounded-full" style="width: 50%"> 50%</div>
</div>
        </div>
    
</div>

</template>

<script setup>
</script>

<style scoped>
h1 {
  text-align: left;
  font-family: 'Style Script', cursive;
  font-weight: 800;
  font-size: 2rem;
  letter-spacing: 4.5px;
  color: var(--text-color);
}



p{
    color: var(--text-color);
    
}

.currentlyContainer {
    margin-left: 7rem; 
    padding-left: 0; 
    margin-top: 7rem;
   
   
}

.progress-bar {
    background-color: #b591b5;
    color: var(--text-color)
}

/* responsive */
@media screen and (max-width: 320px) {
    .currentlyContainer {
    margin: 5rem 0 0 0;
    
  }

  .progress-container {
    width: 100%; 
    margin: 1rem auto; 
  }

  h1 {
    font-size: 1.5rem;
    width: 100%;
    max-width: 20rem;
    text-align: center;
  }

  .progress-bar {
    background-color: #b591b5;
    color: var(--text-color);
  }
  .barContainer {
    width: 100%;
  justify-content: center;
  align-items: center;

  & h3{
    font-size: 1.2rem;
  }

  & p{
   width: 100%;
   font-size: 0.8rem;
   max-width: 18.5rem;
margin-bottom: 1.5rem;

  }

  }

  .overflowBar {
    width: 90%;
  }
 


  
}

@media (min-width: 321px) and (max-width: 480px) {
  .currentlyContainer {
    margin: 5rem 0 0 0;
    
  }

  .progress-container {
    width: 100%; 
    margin: 1rem auto; 
  }

  h1 {
    font-size: 1.5rem;
    width: 100%;
    text-align: center;
  }

  .progress-bar {
    background-color: #b591b5;
    color: var(--text-color);
  }
  .barContainer {
    width: 100%;
  justify-content: center;
  align-items: center;

  & h3{
    font-size: 1.2rem;
   text-align: center;
  }

  & p{
   width: 100%;
   font-size: 0.8rem;
   max-width: 23rem;
margin-bottom: 1.5rem;

  }

  }

  .overflowBar {
    width: 90%;
  } 
}

@media (min-width: 481px) and (max-width: 759px) {
  .currentlyContainer {
    margin: 5rem 0 0 0;
    
  }

  .progress-container {
    width: 100%; 
    margin: 1rem auto; 
  }

  h1 {
    font-size: 2rem;
    width: 100%;
    text-align: center;
  }

  .progress-bar {
    background-color: #b591b5;
    color: var(--text-color);
  }
  .barContainer {
    width: 100%;
  justify-content: center;
  align-items: center;

  & h3{
    font-size: 1.2rem;
   text-align: center;
  }

  & p{
   width: 100%;
   font-size: 0.8rem;
   max-width: 23rem;
margin-bottom: 1.5rem;

  }

  }

  .overflowBar {
    width: 90%;
  } 

}

@media (min-width: 760px) and (max-width: 1024px) {
   
  .currentlyContainer {
    margin: 5rem 0 0 0;
    
  }

  .progress-container {
    width: 100%; 
    margin: 1rem auto; 
  }

  h1 {
    font-size: 2rem;
    width: 100%;
    text-align: center;
  }

  .progress-bar {
    background-color: #b591b5;
    color: var(--text-color);
  }
  .barContainer {
    width: 100%;
  justify-content: center;
  align-items: center;

  & h3{
    font-size: 1.2rem;
   
  }

  & p{
   width: 100%;
   font-size: 0.8rem;
   max-width: 23rem;
margin-bottom: 1.5rem;

  }

  }

  .overflowBar {
    width: 90%;
  }  
}
</style>