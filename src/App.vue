<template>
<NavBar/> 
<HeroSection/>
<SkillsSection/>
<CurrentlyLearning/>
<ProjectsSection/>
<ContactSection/>
<FooterSection/>
</template>

<script setup>
import { onMounted } from 'vue';

import NavBar from './components/NavBar.vue';
import HeroSection from './components/HeroSection.vue';
import SkillsSection from './components/SkillsSection.vue';
import CurrentlyLearning from './components/CurrentlyLearning.vue';
import ProjectsSection from './components/ProjectsSection.vue';
import ContactSection from './components/ContactSection.vue';
import FooterSection from './components/FooterSection.vue'


onMounted(() => {
  document.title = 'Evelyn Nobile - Portfolio';
 
});
</script>


<style lang="scss">


</style>
