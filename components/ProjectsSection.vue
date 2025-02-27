<script setup></script>
<template>
  <section class="projects">
    <h2 class="projects__header">Проекты:</h2>
    <project-card />
    <project-card />
    <project-card />
  </section>
</template>
<style lang="scss">
@use "@/assets/styles/variables.scss" as *;

.projects {
  margin-top: 40px;
  &__header {
    font-size: $font-size-l;
  }
}
</style>
