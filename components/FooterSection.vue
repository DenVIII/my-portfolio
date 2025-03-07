<template>
  <footer>© Denis Vinogradov 2025</footer>
</template>
<style lang="scss">
@use "@/assets/styles/variables.scss" as *;
footer {
  padding: 40px 0;
  margin: 0 auto;
  width: 800px;
  font-family: $font-family-main;
  color: #4c5466;
}

@media (max-width: 768px) {
  footer {
    max-width: 550px;
  }
}

@media (max-width: 440px) {
  footer {
    max-width: 290px;
    padding: 30px 0;
  }
}
</style>
