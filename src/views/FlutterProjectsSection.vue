<template>
  <div class="projectscontainer mt-6">
    <div
      class="flex flex-col justify-items-start my-4 title-container"
      id="projects"
    >
      <h1 class="text-3xl mr-2">Mobile Applications - Flutter</h1>
    </div>
    <div
      class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 mt-12 cardContainer"
    >
      <div
        v-for="project in projects"
        :key="project.name"
        class="project-card overflow-hidden shadow-md w-96 h-full mx-auto"
      >
        <div class="image-container relative w-full h-52">
          <span v-if="project.status" class="status-tag">{{
            project.status
          }}</span>
          <img
            :src="project.img"
            :alt="project.name"
            class="project-image w-full h-full object-cover"
          />
          <div class="overlay">
            <p class="project-description">{{ project.description }}</p>
          </div>
        </div>
        <h2 class="project-title">{{ project.name }}</h2>

        <div
          class="mb-6 flex flex-wrap justify-center align-center gap-4 project-tags"
        >
          <component
            v-for="tag in project.tags"
            :is="getIconComponent(tag)"
            :key="tag"
            class="w-17 h-14"
          ></component>
        </div>
        <div class="project-links mb-4 flex justify-center align-center gap-6">
          <a
            v-if="project.repository"
            :href="project.repository"
            target="_blank"
            >Repository</a
          >
          <a v-if="project.video" :href="project.video" target="_blank"
            >Video</a
          >
          <a v-if="project.link" :href="project.link" target="_blank"
            >Live Demo</a
          >
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";
import { fprojects as projectsData } from "./../flutter_mobile_app.js";

import DartSvg from "@/SVG/DartSvg.vue";
import FlutterSvg from "@/SVG/FlutterSvg.vue";


const projects = ref(projectsData);

const getIconComponent = (tag) => {
  const icons = {
    "Dart": DartSvg,
    "Flutter": FlutterSvg,
  };

  return icons[tag] || null;
};
</script>

<style scoped>
.projectscontainer {
  width: 100%;
  max-width: 1800px;
  margin: 7rem auto 0;
  padding: 0 2rem;
}

.title-container {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
}

h1 {
  text-align: center;
  font-family: "Style Script", cursive;
  font-weight: 800;
  font-size: 2rem;
  letter-spacing: 4px;
  color: var(--text-color);
}

.project-card {
  border: 2px solid var(--text-color);
  border-radius: 15px;
  padding: 0.1rem;
}

.overlay {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: rgba(0, 0, 0, 0.7);
  color: white;
  opacity: 0;
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
  padding: 1rem;
  transition: opacity 0.3s;
  border: 1px solid var(--text-color);
}
.image-container:hover .overlay {
  opacity: 1;
}

.project-title {
  margin: 1rem;
  font-family: "Style Script", cursive;
  letter-spacing: 4px;
  font-size: 1.5rem;
  font-weight: 600;
  text-align: center;
  color: var(--text-color);
}

.project-links {
  color: var(--text-color);
  text-decoration: underline;
}

.status-tag {
  position: absolute;
  top: 15px;
  right: 15px;
  padding: 5px 10px;
  border-radius: 8px;
  font-size: 14px;
  font-weight: bold;
  background-color: var(--lilac-color);
  color: var(--text-color);
  border: 1px solid var(--text-color);
  text-align: center;
}

/* responsive */

@media screen and (max-width: 284px) {
  .overlay {
    padding: 0.5rem;
    font-size: 0.75rem;
    line-height: 1.2rem;
  }
}

@media screen and (max-width: 320px) {
  .projectscontainer {
    flex-direction: column;
    align-items: center;
    justify-content: center;
    margin: 0;
  }

  .title-container {
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    margin-top: 5rem;
  }

  .title-container h1 {
    font-size: 1.5rem;
    width: 100%;
    max-width: 20rem;
    text-align: center;
  }

  .cardContainer {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    width: 100%;
    max-width: 20rem;
    margin-top: 3rem;
  }

  .project-card {
    width: 95%;
    max-width: 20rem;
  }
  .project-description {
    font-size: 13px;
    text-align: center;
    width: 100%;
    max-width: 20rem;
  }
}

@media (min-width: 321px) and (max-width: 480px) {
  .projectscontainer {
    flex-direction: column;
    align-items: center;
    justify-content: center;
    margin: 0;
    max-width: 1800px;
  }

  .title-container {
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    margin-top: 5rem;
  }

  .title-container h1 {
    font-size: 1.5rem;
    width: 100%;
    max-width: 30rem;
    text-align: center;
  }

  .cardContainer {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    width: 100%;
    max-width: 25rem;
    margin-top: 3rem;
    margin-left: auto;
    margin-right: auto;
  }

  .project-card {
    width: 90%;
    max-width: 25rem;
  }

  .project-description {
    font-size: 13px;
    text-align: center;
    width: 100%;
    max-width: 20rem;
  }
}

@media (min-width: 481px) and (max-width: 759px) {
  .projectscontainer {
    flex-direction: column;
    align-items: center;
    justify-content: center;
    margin: 0;
  }

  .title-container {
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    margin-top: 5rem;
  }

  .title-container h1 {
    font-size: 2rem;
    width: 100%;
    max-width: 30rem;
    text-align: center;
  }

  .cardContainer {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    width: 100%;
    max-width: 25rem;
    margin-top: 3rem;
    margin-left: auto;
    margin-right: auto;
  }

  .project-card {
    width: 100%;
    max-width: 25rem;
  }
}

@media (min-width: 760px) and (max-width: 1024px) {
  .projectscontainer {
    flex-direction: column;
    align-items: center;
    justify-content: center;
    margin: 0;
  }

  .title-container {
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    margin-top: 5rem;
  }

  .title-container h1 {
    font-size: 2em;
    width: 100%;
    max-width: 30rem;
    text-align: center;
  }

  .cardContainer {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    width: 100%;
    max-width: 25rem;
    margin-top: 3rem;
    margin-left: auto;
    margin-right: auto;
  }

  .project-card {
    width: 100%;
    max-width: 40rem;
  }
}
</style>
