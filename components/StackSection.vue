<script setup>
import { ref } from "vue";

const stackCardsList = ref([
  {
    title: "HTML5",
    imgSrc: "/image/stack/html-5.svg",
    alt: "HTML5 векторный логотип",
    url: "https://developer.mozilla.org/ru/docs/Web/HTML",
  },
  {
    title: "CSS3",
    imgSrc: "/image/stack/css-3.svg",
    alt: "CSS3 векторный логотип",
    url: "https://developer.mozilla.org/ru/docs/Web/CSS",
  },
  {
    title: "JavaScript",
    imgSrc: "/image/stack/javascript.svg",
    alt: "JavaScript векторный логотип",
    url: "https://developer.mozilla.org/ru/docs/Web/JavaScript",
  },
  {
    title: "Vue.js",
    imgSrc: "/image/stack/vue.svg",
    alt: "Vue.js векторный логотип",
    url: "https://ru.vuejs.org/",
  },
  {
    title: "Nuxt.js",
    imgSrc: "/image/stack/nuxt.svg",
    alt: "Nuxt.js векторный логотип",
    url: "https://nuxt.com/",
  },
  {
    title: "Sass",
    imgSrc: "/image/stack/sass.svg",
    alt: "Sass векторный логотип",
    url: "https://sass-lang.com/",
  },
  {
    title: "ViteJS",
    imgSrc: "/image/stack/vitejs.svg",
    alt: "ViteJS векторный логотип",
    url: "https://vitejs.ru/",
  },
  {
    title: "Webpack",
    imgSrc: "/image/stack/webpack.svg",
    alt: "Webpack векторный логотип",
    url: "https://webpack.js.org/",
  },
  {
    title: "NodeJS",
    imgSrc: "/image/stack/nodejs-3.svg",
    alt: "NodeJS векторный логотип",
    url: "https://nodejs.org/en",
  },
  {
    title: "Express",
    imgSrc: "/image/stack/expressjs-icon.svg",
    alt: "Express векторный логотип",
    url: "https://expressjs.com/",
  },
  {
    title: "PostgreSQL",
    imgSrc: "/image/stack/postgresql.svg",
    alt: "PostgreSQL векторный логотип",
    url: "https://www.postgresql.org/",
  },
  {
    title: "Visual Studio Code",
    imgSrc: "/image/stack/visual-studio-code-1.svg",
    alt: "Visual Studio Code векторный логотип",
    url: "https://code.visualstudio.com/",
  },
  {
    title: "Adobe Photoshop",
    imgSrc: "/image/stack/adobe-photoshop.svg",
    alt: "Adobe Photoshop векторный логотип",
    url: "https://www.adobe.com/",
  },
  {
    title: "Adobe Illustrator",
    imgSrc: "/image/stack/adobe-illustrator.svg",
    alt: "Adobe Illustrator векторный логотип",
    url: "https://www.adobe.com/",
  },
]);
</script>

<template>
  <section class="stack">
    <h2 class="stack__header">Мои навыки:</h2>
    <ul class="stack__list">
      <stack-card
        v-for="stackCard in stackCardsList"
        :key="`data-id-${stackCard.title}`"
        :data="stackCard"
      ></stack-card>
    </ul>
  </section>
</template>
<style lang="scss">
@use "@/assets/styles/variables.scss" as *;

.stack {
  &__header {
    font-size: $font-size-l;
    margin-bottom: 60px;
  }
  &__list {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    row-gap: 40px;
    column-gap: 20px;
  }
}
</style>
