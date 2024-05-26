<template>
    <footer>
        <div class="infoContainer">
            <a href="https://www.linkedin.com/in/evelyn-nobile/" target="_blank" rel="noopener noreferrer" class="linkGithub"><ph-linkedin-logo :size="20" weight="fill"/></a>
            <a href="mailto:nobileevelyn1@gmail.com" target="_blank" rel="noopener noreferrer" class="linkGithub"><ph-envelope-simple :size="20" weight="fill" /></a>
            <a href="https://wa.me/+541154046884" target="_blank" rel="noopener noreferrer" class="linkGithub"><ph-whatsapp-logo :size="20" weight="fill" /></a>
            <a href="https://github.com/Evelyn-Nobile" target="_blank" rel="noopener noreferrer" class="linkGithub"><ph-github-logo :size="20" weight="fill" /></a>
        </div>
        
           <p class="mt-5 text-sm">@2024 Evelyn Nobile - All rights reserved.</p>
    </footer>
</template>

<script setup>
import { PhLinkedinLogo, PhEnvelopeSimple, PhWhatsappLogo,PhGithubLogo } from '@phosphor-icons/vue'
</script> 

<style scoped>

footer {
    width: 100%;
    height: 10vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.2);
    background-color: #ecdfeb;
    margin-top: 4rem;
}

.infoContainer {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 1rem;
    color: var(--text-color);
    cursor: pointer;
}

/* responsive */

@media screen and (max-width: 320px) {
   
}

</style>