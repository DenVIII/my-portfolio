<script setup>
import { ref } from "vue";

const projectsData = ref([
  {
    title: "Портфолио для 3D-визуализатора",
    imgSrc: "/image/project-1.jpg",
    url: "#",
    git: "https://github.com/DenVIII/kris-vin-3d-visualizer-portfolio",
  },
  {
    title: "База данных для доставки продуктов питания",
    imgSrc: "/image/project-2.jpg",
    url: "https://github.com/DenVIII/inventory-app",
    git: "https://github.com/DenVIII/inventory-app",
  },
  {
    title: "Сайт-портфолио для 3D-визуализатора",
    imgSrc: "/image/project-1.jpg",
    url: "https://github.com/DenVIII/inventory-app",
    git: "https://github.com/DenVIII/kris-vin-3d-visualizer-portfolio",
  },
]);
</script>

<template>
  <section class="projects">
    <h2 class="projects__header">Проекты:</h2>
    <project-card
      v-for="project in projectsData"
      :key="`Project-id-${project.title}`"
      :project="project"
    />
  </section>
</template>
<style lang="scss">
@use "@/assets/styles/variables.scss" as *;

.projects {
  margin-top: 40px;
}
</style>
