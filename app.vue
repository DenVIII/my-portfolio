<template>
  <Html>
    <Head>
      <Link
        rel="preconnect"
        href="https://fonts.googleapis.com"
      />
      <Link
        rel="preconnect"
        href="https://fonts.gstatic.com"
        crossorigin
      />
      <Link
        href="https://fonts.googleapis.com/css2?family=Roboto+Condensed:ital,wght@0,100..900;1,100..900&family=Ubuntu:ital,wght@0,300;0,400;0,500;0,700;1,300;1,400;1,500;1,700&display=swap"
        rel="stylesheet"
      />
    </Head>
  </Html>
  <nav-bar />
  <main class="content">
    <NuxtPage />
  </main>
  <footer-section />
</template>

<style lang="scss">
@use "./assets/styles/main.scss";
</style>
