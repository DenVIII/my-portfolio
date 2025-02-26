<script setup></script>
<template>
  <section class="hero">
    <p class="hero__descr">Привет, меня зовут Денис, моя профессия:</p>
    <h1 class="hero__header">
      <span class="hero__text_reduced_size">&lt;</span>веб-разработчик
      <span class="hero__text_reduced_size">/&gt;</span>
      <span class="hero__text-cursor">|</span>
    </h1>
    <a href="#"><button class="hero__contact-btn">Связаться со мной</button></a>
  </section>
</template>
<style lang="scss">
@use "@/assets/styles/variables.scss" as *;

.hero {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 100vh;
  position: relative;
  &__header {
    font-size: $font-size-xl;
    margin-bottom: 15px;
  }
  &__text_reduced_size {
    font-size: 0.75em;
  }
  &__contact-btn {
    color: $background-color;
    background-color: $primary-color;
    font-size: 1rem;
  }
  &__descr {
    font-weight: 300;
    font-size: 1rem;
  }
  &__text-cursor {
    color: $secondary-color;
  }
  &::after {
    content: "";
    position: absolute;
    z-index: -1;
    width: 100vw;
    height: 100vh;
    background-color: transparent;

    /* Создаем точки */
    background-image: radial-gradient($secondary-color, 1px, transparent 0);
    background-size: 20px 20px;
    background-position: 0 0, 10px 10px;

    /* Добавляем эффект размытия по краям */
    mask-image: radial-gradient(
      circle at center,
      rgba(255, 255, 255, 1) 0%,

      rgba(255, 255, 255, 0.5) 70%,
      rgba(255, 255, 255, 0) 100%
    );

    /* Альтернативный способ через clip-path для старых браузеров */
    -webkit-clip-path: radial-gradient(
      circle at center,
      rgba(255, 255, 255, 1) 0%,
      rgba(255, 255, 255, 0.6) 30%,
      rgba(255, 255, 255, 0.2) 70%,
      rgba(255, 255, 255, 0) 100%
    );
    clip-path: radial-gradient(
      circle at center,
      rgba(255, 255, 255, 1) 0%,
      rgba(255, 255, 255, 0.6) 30%,
      rgba(255, 255, 255, 0.2) 70%,
      rgba(255, 255, 255, 0) 100%
    );
  }
}
</style>
