<template>
  <nav class="navbar">
    <a
      href="#home"
      class="navbar__link"
      id="logo"
      >Denis V.</a
    >
    <a
      href="#contacts"
      class="navbar__link"
      >Контакты</a
    >
  </nav>
</template>

<style lang="scss">
@use "@/assets/styles/variables.scss" as *;
.navbar {
  position: fixed;
  top: 0;
  z-index: 99;
  height: 60px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  max-width: 1120px;
  left: 0;
  right: 0;
  margin: 0 auto;
  padding: 40px 0;
  &__link {
    &:hover {
      text-decoration: underline;
    }
  }
}
</style>
