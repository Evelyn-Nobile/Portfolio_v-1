<template>
  <div class="contactContainer flex items-center justify-center flex-col rounded-xl mx-auto py-6"> 
    <div class="w-1/2 flex items-center justify-center contactContent">
      <img src="https://avatars.githubusercontent.com/u/102312214?v=4" alt="github-avatar" class="rounded-lg w-48 h-35">
      <div class="p-6 contacttextsContainer">
        <h2 class="text-4xl">Contact</h2>
        <p class="text-justify mt-4 herotext">If you are looking to work with a person who is passionate about technology, curious, proactive, with a great capacity for learning and responsible... Eureka! you have found it 😉</p>
        <div class="mt-6 flex gap-6 justify-start items-start">
          <button class="buttons flex items-center justify-center p-3 rounded-xl gap-1">
            <ph-linkedin-logo :size="20" weight="fill"/><a href="https://www.linkedin.com/in/evelyn-nobile/" target="_blank" rel="noopener noreferrer" class="linkGithub">LinkedIn</a>
          </button>
          <button class="buttons flex items-center justify-center p-3 rounded-xl gap-1">      
            <ph-envelope-simple :size="20" weight="fill" /><a href="mailto:nobileevelyn1@gmail.com" target="_blank" rel="noopener noreferrer" class="linkGithub">Mail me</a>
          </button>
          <button class="buttons flex items-center justify-center p-3 rounded-xl gap-1">
            <ph-whatsapp-logo :size="20" weight="fill" /><a href="https://wa.me/+541154046884?text=Hola,%20tengo%20una%20oferta%20que%20podría%20interesarte." target="_blank" rel="noopener noreferrer" class="linkGithub">Let's chat?</a>
          </button>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { PhLinkedinLogo, PhEnvelopeSimple, PhWhatsappLogo } from '@phosphor-icons/vue'
</script>

<style scoped>
.contactContainer {
  width: 1000px;
  background-color: #08030C;
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
  color: var(--stress-color);
}

a:hover {
  color: #e0b0ff;
}

.buttons {
  background-color: var(--main-color);
  color: var(--text-color);
  width: 9rem;
  font-size: 0.8rem;
  text-align: center;
  display: flex; /* Para centrar el contenido */
  justify-content: center; /* Para centrar el contenido */
  align-items: center; /* Para centrar el contenido */
}

.buttons:hover {
  background-color: #7f00b2;
}

/* responsive: */
@media (min-width: 760px) and (max-width: 1023px) {
  .contactContainer {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    margin-top: 2rem;
  }

  p {
    max-width: 350px;
  }
}

@media screen and (max-width: 759px) {
  .contacttextsContainer {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }

  p,
  h2,
  span,
  a {
    width: 350px;
  }

  .contactContent {
    display: flex;
    flex-direction: column;
  }

  .buttons {
    width: 160px;
    text-align: center;
  }

  a {
    display: flex;
    justify-content: center;
    align-items: center;
  }
}
</style>
