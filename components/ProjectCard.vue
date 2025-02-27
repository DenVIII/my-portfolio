<script setup></script>
<template>
  <div class="project-card">
    <div class="project-card__image">
      <div class="mask">
        <div class="container">
          <p class="project-card__description">
            Портфолио для 3D-визуализатора
          </p>
          <div class="project-card__btns">
            <a href="#">
              <button>
                <img
                  class="project-card__icon"
                  src="/image/github-mark.svg"
                  alt="Ссылка на гитхаб"
                />
              </button>
            </a>
            <a href="#">
              <button>
                <img
                  class="project-card__icon"
                  src="/image/redirect-icon.png"
                  alt="Ссылка на сайт"
                />
              </button>
            </a>
          </div>
        </div>
      </div>
      <img
        src="/image/project-1.jpg"
        class="project-card__background"
        alt=""
      />
    </div>
  </div>
</template>

<style lang="scss">
@use "@/assets/styles/variables.scss" as *;

.project-card {
  .container {
    display: flex;
    justify-content: space-between;
    margin-bottom: 60px;
    align-items: center;
  }
  &__image {
    margin: 60px 0;
    max-height: 400px;
    position: relative;
    display: block;
    overflow: hidden;
    border-radius: $border-radius-s;
    transition: all 0.5s ease;
  }

  &__background {
    width: 100%;
    height: 100%;
    object-fit: cover;
    border-radius: $border-radius-s;
    vertical-align: middle;
    z-index: -1;
  }

  &__image:hover {
    cursor: pointer;
    transform: scale(0.95);
    outline-color: $background-color;
    img {
      transform: scale(1.15);
    }
  }

  &__image:hover > .mask {
    transform: translateY(0);
  }

  &__description {
    color: $background-color;
    font-size: $font-size-n;
    font-family: $font-family-main;
    opacity: 1;
  }

  &__btns {
    display: flex;
    gap: 20px;
  }

  &__icon {
    width: 24px;
    height: 24px;
  }

  &__icon:hover {
    cursor: pointer;
  }

  .mask {
    position: absolute;
    padding: 20px 40px;
    background-color: hsla(240, 8%, 3%, 0.3);
    transform: translateY(-100%);
    height: 400px;
    width: 100%;
    z-index: 1;
    display: flex;
    flex-direction: column;
    justify-content: end;
  }
}
</style>
