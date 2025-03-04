<script setup>
import { defineProps } from "vue";

defineProps({
  data: {
    type: Object,
    required: true,
  },
});
</script>
<template>
  <li>
    <a
      :href="data.url"
      target="_blank"
      class="logo"
    >
      <div class="logo__wrapper">
        <div class="logo__container">
          <img
            class="logo__img"
            :src="data.imgSrc"
            :alt="data.alt"
          />
        </div>
        <p class="logo__title">{{ data.title }}</p>
      </div>
    </a>
  </li>
</template>
<style lang="scss" scoped>
@use "@/assets/styles/variables.scss" as *;

.logo {
  position: relative;
  display: block;
  width: 140px;
  height: 140px;
  &__img {
    width: 100px;
    height: 100px;
  }
  &__container {
    display: flex;
    height: 80%;
    padding-top: 10px;
    justify-content: center;
    align-items: center;
  }
  &__title {
    padding: 10px 5px;
    font-size: $font-size-s;
    font-weight: 300;
    text-align: center;
  }
  /*  &::before {
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: radial-gradient(circle, #f8f9fa 45%, #92e0ff 100%);
    background-size: 150% 150%;
    background-position: 100% 100%;
    opacity: 0;
    filter: blur(0);
    z-index: -1;
    transition: opacity 0.5s ease, filter 0.5s ease,
      background-position 1.5s ease;
  }
  &:hover {
    box-shadow: 5px 5px 20px 0 #9cc2d1;
  }
  &:hover::before {
    opacity: 0.6;
    filter: blur(5px);
    background-position: 0 0;
  } */
}
</style>
