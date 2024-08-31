<script setup>
import Header from './components/PageHeader.vue'
import Contents from './components/SiteContents.vue'
import SectionAbout from './components/SectionAbout.vue'
import SectionSkills from './components/SectionSkills.vue'
import SectionExperience from './components/SectionExperience.vue'
import SectionProjects from './components/SectionProjects.vue'
</script>

<template>
  <div class="page">
    <div class="sidebar">
      <Header name="Dina Shoham" title="Software Engineer"></Header>
      <br />
      <Contents
        :items="[
          { text: 'About', id: 'about' },
          { text: 'Experience', id: 'experience' },
          { text: 'Skills', id: 'skills' },
          { text: 'Projects', id: 'projects' }
        ]"
      >
      </Contents>
    </div>
    <div class="content">
      <div class="section" id="about">
        <SectionAbout></SectionAbout>
      </div>
      <hr />
      <div class="section" id="experience">
        <SectionExperience></SectionExperience>
      </div>
      <hr />
      <div class="section" id="skills">
        <SectionSkills></SectionSkills>
      </div>
      <hr />
      <div class="section" id="projects">
        <SectionProjects></SectionProjects>
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

/*red horiz lines*/
hr {
  display: block;
  height: 1px;
  border: 0;
  border-top: 1px solid var(--accent-color);
  margin: 0rem 1rem 2rem 1rem;
  padding: 0;
}

/* .container:hover {
  background-color: var(--hover-color);
} */
</style>
