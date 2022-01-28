<template>
  <header>
    <nav class="header__nav" aria-label="top">
      <div class="header__menu">
        <a href="#">
          <span class="sr-only">Workflow</span>
          <img
            class="w-auto h-10"
            src="https://tailwindui.com/img/logos/workflow-mark.svg?color=white"
            alt
          />
        </a>
        <div class="header__list">
          <a href="#" class="header__link header__link--black">Home</a>
          <a href="#" class="header__link header__link--black">Contato</a>
        </div>
      </div>
      <div class="box">
        <div class="box__title">Giovanni Franco</div>
        <div class="box__project">
          <span class="box__link">Projetos</span>
        </div>
      </div>
    </nav>
  </header>
  <main></main>
  <footer></footer>
</template>

<script>
export default {
  name: 'App',
}
</script>

<style lang="postcss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
header {
  background-image: url("assets/images/women-pixel-art-4k-98.jpg");
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center center;
  @apply h-screen relative;
}

/* .header__nav {
  @apply max-w-7xl mx-auto;
} */
.header__menu {
  @apply flex  py-5 px-3 justify-between lg:border-none;
  @apply w-full items-center;
}
.header__link {
  @apply inline-block px-4 py-2 text-base font-semibold relative;
  @apply transition-colors w-32 text-center;
  @apply transition-opacity;
  @apply hover:border-opacity-90;
}
.header__link::after {
  content: "";
  @apply absolute w-0 h-0.5 bg-current transition-opacity;
  @apply block ease-in transition-all;
}
.header__link:hover::after {
  @apply w-4/5;
}
.header__list {
  @apply flex gap-3 justify-end;
}
.header__link--black {
  @apply text-black;
  @apply hover:bg-opacity-75 transition-shadow;
}

.header__link--white {
  @apply text-indigo-600 bg-white;
  @apply hover:bg-indigo-50;
}
.box {
  @apply absolute top-1/2 left-1/2  w-1/2 -translate-x-1/2 -translate-y-1/2;
}
.box__link {
  @apply border text-center relative border-white rounded-xl text-white font-semibold text-lg py-3 overflow-hidden;
  @apply transition-all hover:text-black;
}
.box__link::before {
  content: "";
  transition: 0.2s ease-in-out all;
  border-radius: 0 0 50% 50%;
  @apply absolute top-0 left-0 h-0 w-full bg-white -z-10;
}
.box__link:hover::before {
  @apply h-20;
}

.box__title {
  @apply lg:text-5xl md:text-4xl text-white font-semibold text-center mb-3;
}
.box__project {
  @apply w-56 mx-auto flex justify-center  cursor-pointer relative overflow-hidden;
  @apply hover:shadow-sm;
}
</style>
