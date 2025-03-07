<script setup></script>
<template>
  <section
    class="contacts"
    id="contacts"
  >
    <h2 class="contacts__header">Будем на связи:</h2>
    <div class="contacts__wrapper">
      <a
        href="mailto:denis226@list.ru"
        class="contacts__social"
        >denis226@list.ru</a
      >
      <a
        href="https://vk.com/id__13_37"
        class="contacts__social"
        >Вконтакте</a
      >
      <a
        href="https://t.me/DenVIII"
        class="contacts__social"
        >Телеграмм</a
      >
    </div>
  </section>
</template>
<style lang="scss">
@use "@/assets/styles/variables.scss" as *;

.contacts {
  margin: 140px 0;
  &__header {
    margin-bottom: 20px;
    font-size: 1.5rem;
  }
  &__social {
    display: block;
    font-size: $font-size-l;
    font-family: $font-family-header;
  }
  &__social:hover {
    color: $secondary-color;
  }
}

@media (max-width: 768px) {
  .contacts {
    margin: 80px 0;
    &__header {
      font-size: 1.2rem;
    }
    &__social {
      font-size: 2rem;
    }
  }
}
@media (max-width: 768px) {
  .contacts {
    margin: 50px 0;
  }
}
</style>
