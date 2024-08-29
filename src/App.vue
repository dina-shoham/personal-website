<script setup>
import Header from './components/PageHeader.vue'
import SectionAbout from './components/SectionAbout.vue'
import SectionSkills from './components/SectionSkills.vue'
import SectionExperience from './components/SectionExperience.vue'
import Contents from './components/SiteContents.vue'
</script>

<template>
  <div class="page">
    <div class="sidebar">
      <Header name="Dina Shoham" title="Software Engineer"></Header>
      <br />
      <Contents
        :items="[
          { text: 'About', id: 'about' },
          { text: 'Skills', id: 'skills' },
          { text: 'Experience', id: 'experience' }
        ]"
        :value="true"
      >
      </Contents>
    </div>
    <div class="content">
      <div class="section" id="about">
        <SectionAbout></SectionAbout>
      </div>
      <div class="section" id="skills">
        <SectionSkills></SectionSkills>
      </div>
      <div class="section" id="experience">
        <SectionExperience></SectionExperience>
      </div>
    </div>
  </div>
</template>

<style scoped>
@import 'assets/main.css';

.sidebar {
  width: 15rem;
  padding: 1rem;
  position: fixed;
  height: 100%;
  overflow: auto;
}

.content {
  margin-left: 17rem;
  padding: 1rem;
  overflow-x: hidden;
}

.section {
  padding: 0rem 1rem 2rem 1rem; /*top right bottom left*/
}

/* .container:hover {
  background-color: var(--hover-color);
} */
</style>
