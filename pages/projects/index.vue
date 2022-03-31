<template>
  <div>
    <Content>
      <Project
      v-for="(project, i) in projects"
      :key="i"
      :title="project.title"
      :desc="project.desc"
      :img="project.img" />
    </Content>
  </div>
</template>

<script>
import Project from '@/components/Project.vue'

export default {
  Project,
  data() {
    return {
      projects: [
        {
          title: 'project 1',
          desc: 'desc for project 1',
          img: [ 'test_img1.png', 'test_img2.png', 'test_img3.png' ]
        },
        {
          title: 'project 2',
          desc: 'desc for project 2',
          img: [ 'test_img1.png', 'test_img2.png', 'test_img3.png' ]
        }
      ]
    }
  }
}
</script>