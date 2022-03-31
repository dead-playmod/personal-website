<template>
  <header class="text-white w-screen z-50 bg-black h-20">
    <nav class="w-full h-full flex flex-row">
      <div class="flex flex-grow h-full">
        <nuxt-link to="/" class="h-20 w-20 flex justify-center items-center logo">
          <span class="text-6xl">:3</span>
        </nuxt-link>
      </div>
      <ul class="flex max-w-min items-center text-lg">
        <li>
          <nuxt-link to="/">Home</nuxt-link>
        </li>
        <li>
          <nuxt-link to="/about">About</nuxt-link>
        </li>
        <li>
          <nuxt-link to="/projects">Projects</nuxt-link>
        </li>
      </ul>
    </nav>
  </header>
</template>
<script>
export default {
  name: 'Header'
}
</script>

<style scoped>
.logo > span {
  transition: transform 0.4s ease-out, text-shadow 0.45s ease-out;
}
.logo:hover > span {
  transform: scale(1.1) rotateZ(15deg);
  text-shadow: 0 0 10px white;
}
li
{
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  margin: 0 1.5rem;
}
li > a {
  padding: 0.5rem 1rem;
  transition: background-position-y 0.4s ease, border-bottom 0.3s ease, transform 0.6s ease;
  background: linear-gradient(0deg, rgba(154,0,255,1) -50%, rgba(0,0,0,0) 50%);
  border-bottom: rgba(210, 0, 252, 0) solid 1px;
  background-repeat: no-repeat;
  background-position-y: 25px;
}
li > a:hover {
  background-position-y: 0;
  transform: translateY(-5px);
  border-bottom: rgba(210, 0, 252, 0.75) solid 1px;
}
</style>