<template>
  <div class="w-3/4 mx-auto my-20 p-9 rounded-xl flex border border-solid">
    <div class="w-5/12 m-3 relative flex items-center overflow-hidden img-gallery">
      <button 
        class="arrow-left"
        @click="() => {
          if(imgIndex > 0)
            imgIndex--;
          else
            imgIndex = this.img.length - 1;
        }"
      >
        <font-awesome-icon icon="fa-solid fa-chevron-left" />
      </button>
      
      <img 
        :src="require(`@/assets/img/${img[imgIndex]}`)" 
        alt="project image"
        class="rounded"
      >

      <button 
        class="arrow-right"
        @click="() => {
          if(imgIndex < this.img.length - 1)
            imgIndex++;
          else
            imgIndex = 0;
        }"
      >
        <font-awesome-icon icon="fa-solid fa-chevron-right" />
      </button>
    </div>

    <div class="w-7/12 ml-5 flex flex-col">
      <h1 class="text-4xl font-semibold text-center">{{ title }}</h1>

      <p class="text-lg flex-grow">{{ desc }}</p>

      <a 
        href="https://www.google.com/" 
        class="flex justify-end"
      >
        <font-awesome-icon icon="fa-solid fa-link" size="xl" />
      </a>
    </div>
  </div>
</template>

<script>
import Vue from 'vue';

import { library } from '@fortawesome/fontawesome-svg-core';
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome';

import { faChevronLeft } from '@fortawesome/free-solid-svg-icons';
import { faChevronRight } from '@fortawesome/free-solid-svg-icons';
import { faLink } from '@fortawesome/free-solid-svg-icons';

library.add(faChevronRight, faChevronLeft, faLink);

Vue.component('font-awesome-icon', FontAwesomeIcon);
Vue.config.productionTip = false;


export default {
  name: 'project',
  props: {
    title: String,
    desc: String,
    img: Array
  },
  data() {
    return {
      imgIndex: 0
    }
  }
}
</script>

<style scoped>
.arrow-left,
.arrow-right {
  position: absolute;
  height: 100%;
  width: 3rem;
  transition: 350ms ease-out;
}

.arrow-left {
  left: -3rem;
  background: linear-gradient(90deg, rgba(0,0,0,0.6) 0%, rgba(0,0,0,0) 90%);
}
.arrow-right {
  right: -3rem;
  background: linear-gradient(270deg, rgba(0,0,0,0.6) 0%, rgba(0,0,0,0) 90%);
}

.img-gallery:hover > .arrow-left {
  left: 0;
}
.img-gallery:hover > .arrow-right {
  right: 0;
}

svg {
  transition: transform 0.3s ease-out, filter 0.4s ease-out;
}
svg:hover, button:hover > svg {
  transform: scale(1.2);
  filter: drop-shadow(0 0 2px white);
}
</style>