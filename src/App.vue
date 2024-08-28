<script setup>
import Header from './components/Header.vue'
import SectionAbout from './components/SectionAbout.vue'
import SectionSkills from './components/SectionSkills.vue'
import SectionExperience from './components/SectionExperience.vue'
</script>

<template>
  <div class="page">
    <div class="sidebar">
      <Header name="Dina Shoham" title="Software Engineer"></Header>
    </div>
    <div class="content">
      <div class="section">
        <SectionAbout></SectionAbout>
      </div>
      <div class="section">
        <SectionSkills></SectionSkills>
      </div>
      <div class="section">
        <SectionExperience></SectionExperience>
      </div>
    </div>
  </div>
</template>

<style scoped>
.sidebar {
  margin: 0;
  padding: 0;
  width: 15rem;
  position: fixed;
  height: 100%;
  overflow: auto;
}

.content {
  margin-left: 15rem;
  padding: 1.5rem 1rem 2rem 2rem;
}

.section {
  padding: 0rem 1rem 2rem 1rem; /*top right bottom left*/
}
</style>
