<template>
  <section class="contactContainer flex items-center justify-center flex-col rounded-xl mx-auto py-6" id="contact"> 
    <div class="w-1/2 flex items-center justify-center contactContent">
      <img src="https://res.cloudinary.com/dpxrcotbh/image/upload/v1716711674/zuo4fyoaok9zmknet8ug.webp" alt="profile" class="rounded-lg  profile-img">
      <div class="p-6 contacttextsContainer">
        <h2 class="text-4xl">Contact me...</h2>
        <p class="text-justify mt-4 herotext">If you are looking to work with a person who is passionate about technology, curious, proactive, with a great capacity for learning and responsible... Eureka! you have found it 😉</p>
        <div class="mt-6 flex gap-6 justify-start items-start buttonsContainer">
          <button class="buttons flex items-center justify-center p-3 rounded-xl gap-1 button-pink">
            <ph-linkedin-logo :size="20" weight="fill"/><a href="https://www.linkedin.com/in/evelyn-nobile/" target="_blank" rel="noopener noreferrer" class="linkGithub">LinkedIn</a>
          </button>
          <button class="buttons flex items-center justify-center p-3 rounded-xl gap-1 button-lilac">      
            <ph-envelope-simple :size="20" weight="fill" /><a href="mailto:nobileevelyn1@gmail.com" target="_blank" rel="noopener noreferrer" class="linkGithub">Mail me</a>
          </button>
          <button class="buttons flex items-center justify-center p-3 rounded-xl gap-1 button-pink">
            <ph-whatsapp-logo :size="20" weight="fill" /><a href="https://wa.me/+541154046884" target="_blank" rel="noopener noreferrer" class="linkGithub">Let's chat?</a>
          </button>
        </div>
      </div>
    </div>
  </section>

</template>

<script setup>
import { PhLinkedinLogo, PhEnvelopeSimple, PhWhatsappLogo } from '@phosphor-icons/vue'
</script>

<style scoped>
.contactContainer {
  width: 1000px;
  border: 1px solid var(--text-color);
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  margin-top: 7rem;
}

.contacttextsContainer {
  width: 100%;
}

p {
  width: 500px;
}

span,
p,
a {
  color: var(--text-color);
}

h2 {
font-family: 'style script', cursive;
font-weight: 500;
letter-spacing: 4px;
text-align: center;
}



.buttons {
  color: var(--text-color);
  width: 9rem;
  font-size: 0.8rem;
  text-align: center;
  display: flex; 
  justify-content: center; 
  align-items: center; 
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

.profile-img {
width: 80%;
margin-top: 2rem;
}
/* responsive: */

@media screen and (max-width: 320px) {
  .contactContainer {
  width: 100%;
  border: 1px solid var(--text-color);
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  margin-top: 5rem;
}

.contacttextsContainer {
  width: 100%;
}
.buttonsContainer {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.contactContent {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  width: 100%;
}
p {
  width: 100%;
  max-width: 20rem;
}



h2 {
  font-size: 2rem;
}



.buttons {
  color: var(--text-color);
  width: 9rem;
  font-size: 0.8rem;
  text-align: center;
  display: flex; 
 
  justify-content: center; 
  align-items: center; 
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

.profile-img {
width: 80%;
margin-top: 2rem;
}   
  }
  
  @media (min-width: 321px) and (max-width: 480px) {

    .contactContainer {
  width: 95%;
  border: 1px solid var(--text-color);
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  margin-top: 5rem;
}

.contacttextsContainer {
  width: 100%;
}
.buttonsContainer {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.contactContent {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  width: 100%;
}
p {
  width: 100%;
  max-width: 30rem;
}



h2 {
  font-size: 2rem;
}



.buttons {
  color: var(--text-color);
  width: 9rem;
  font-size: 0.8rem;
  text-align: center;
  display: flex; 
 
  justify-content: center; 
  align-items: center; 
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

.profile-img {
width: 80%;
margin-top: 2rem;
}    
  }

 @media screen and (min-width: 448px) {

 .buttonsContainer{
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
 }


 


 } 
  
  @media (min-width: 481px) and (max-width: 759px) {
    .contactContainer {
  width: 95%;
  border: 1px solid var(--text-color);
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  margin-top: 5rem;
}

.contacttextsContainer {
  width: 100%;
}
.buttonsContainer {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.contactContent {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  width: 100%;
}
p {
  width: 100%;
  max-width: 30rem;
}



h2 {
  font-size: 2rem;
}


.buttonsContainer{
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
 }

.buttons {
  color: var(--text-color);
  width: 9rem;
  font-size: 0.8rem;
  text-align: center;
  display: flex; 
  justify-content: center; 
  align-items: center; 
  position: relative;
  transition: box-shadow 0.3s ease;
  border: 1px solid var(--text-color);
}

.profile-img {
width: 80%;
margin-top: 2rem;
}  
  }
  
  @media (min-width: 760px) and (max-width: 1024px) {
        .contactContainer {
  width: 95%;
  border: 1px solid var(--text-color);
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  margin-top: 5rem;
}

.contacttextsContainer {
  width: 100%;
}
.buttonsContainer {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.contactContent {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  width: 100%;
}
p {
  width: 100%;
}



h2 {
  font-size: 2rem;
}


.buttonsContainer{
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
 }
 
.buttons {
  color: var(--text-color);
  width: 9rem;
  font-size: 0.8rem;
  text-align: center;
  display: flex; 
  justify-content: center; 
  align-items: center; 
  position: relative;
  transition: box-shadow 0.3s ease;
  border: 1px solid var(--text-color);
}

.profile-img {
width: 80%;
margin-top: 2rem;
}  
  
  }


</style>
