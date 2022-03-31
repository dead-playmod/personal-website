<template>
  <div>
    <Header />
    <Nuxt />
  </div>
</template>

<style scoped>
@keyframes header-slide {
  0% {
    opacity: 0;
    transform: translateY(-100%);
  }
  60% {
    opacity: 0;
    transform: translateY(-100%);
  }
  100% {
    opacity: 1;
    transform: translateY(0);
  }
}
Header {
  animation-name: header-slide;
  animation-duration: 2.75s;
  animation-timing-function: ease-out;
}
</style>