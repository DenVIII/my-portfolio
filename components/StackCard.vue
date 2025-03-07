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
}

@media (max-width: 768px) {
  .logo {
    width: 110px;
    height: 110px;
    &__img {
      width: 70px;
      height: 70px;
    }
  }
}

@media (max-width: 440px) {
  .logo {
    width: 70px;
    height: 70px;
    &__img {
      width: 40px;
      height: 40px;
    }
  }
}
</style>
