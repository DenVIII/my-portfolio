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

@media (max-width: 1024px) {
  .navbar {
    max-width: 980px;
  }
}

@media (max-width: 768px) {
  .navbar {
    max-width: 740px;
    margin: 0 auto;
  }
}

@media (max-width: 440px) {
  .navbar {
    max-width: 100%;
    margin: 0 auto;
    padding: 20px;
  }
}
</style>
