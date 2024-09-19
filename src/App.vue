<template> 
<NavBar/> 
<HeroSection/>
<SkillsSection/>
<CurrentlyLearning/>
<ProjectsSection/>
<FlutterProjectsSection/>
<ContactSection/>
<FooterSection/>

</template>

<script setup>
import { onMounted } from 'vue';

import NavBar from './components/NavBar.vue';
import HeroSection from './views/HeroSection.vue';
import SkillsSection from './views/SkillsSection.vue';
import CurrentlyLearning from './views/CurrentlyLearning.vue';
import ProjectsSection from './views/ProjectsSection.vue';
import ContactSection from './views/ContactSection.vue';
import FooterSection from './components/FooterSection.vue'
import FlutterProjectsSection from './views/FlutterProjectsSection.vue';


onMounted(() => {
  document.title = 'Evelyn Nobile - Portfolio';
 
});
</script>


<style lang="scss">


</style>
