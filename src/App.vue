<script setup>
import Header from './components/PageHeader.vue'
import Contents from './components/SiteContents.vue'
import SectionAbout from './components/SectionAbout.vue'
import SectionSkills from './components/SectionSkills.vue'
import SectionExperience from './components/SectionExperience.vue'
import SectionProjects from './components/SectionProjects.vue'
import LanguageToggle from './components/LanguageToggle.vue'

import { ref } from 'vue'

const isFrench = ref(false)
</script>

<template>
  <div class="page">
    <!-- headers/sidebars -->
    <!-- mobile header (title + headline + lang toggle) -->
    <div class="header-mobile">
      <div>
        <Header :is-french="isFrench"></Header>
        <br />
        <LanguageToggle v-model="isFrench" />
        <br />
      </div>
      <hr class="hr-desktop" />
    </div>
    <!-- desktop sidebar (title + headline + contents + lang toggle) -->
    <div class="sidebar-desktop">
      <Header :is-french="isFrench"></Header>
      <br />
      <Contents
        :is-french="isFrench"
        :items="[
          { textEN: 'About', textFR: 'À Propos', id: 'about' },
          { textEN: 'Experience', textFR: 'Expérience', id: 'experience' },
          { textEN: 'Skills', textFR: 'Compétences', id: 'skills' },
          { textEN: 'Projects', textFR: 'Projets', id: 'projects' }
        ]"
      >
      </Contents>
      <br />
      <LanguageToggle v-model="isFrench" />
    </div>

    <!-- content -->
    <div class="content">
      <!-- about -->
      <div class="section" id="about">
        <div class="mobile-section-header">
          <h2 v-show="!isFrench"><span>About</span></h2>
          <h2 v-show="isFrench"><span>À Propos</span></h2>
        </div>
        <SectionAbout :is-french="isFrench"></SectionAbout>
      </div>
      <!-- line -->
      <hr class="hr-desktop" />
      <!-- experience -->
      <div class="section" id="experience">
        <div class="mobile-section-header">
          <h2 v-show="!isFrench"><span>Experience</span></h2>
          <h2 v-show="isFrench"><span>Expérience</span></h2>
        </div>
        <SectionExperience :is-french="isFrench"></SectionExperience>
      </div>
      <!-- line -->
      <hr class="hr-desktop" />
      <!-- skills -->
      <div class="section" id="skills">
        <div class="mobile-section-header">
          <h2 v-show="!isFrench"><span>Skills</span></h2>
          <h2 v-show="isFrench"><span>Compétences</span></h2>
        </div>
        <SectionSkills :is-french="isFrench"></SectionSkills>
      </div>
      <!-- line -->
      <hr class="hr-desktop" />
      <!-- projects -->
      <div class="section" id="projects">
        <div class="mobile-section-header">
          <h2 v-show="!isFrench"><span>Projects</span></h2>
          <h2 v-show="isFrench"><span>Projets</span></h2>
        </div>
        <SectionProjects :is-french="isFrench"></SectionProjects>
      </div>
    </div>
  </div>
</template>

<style scoped>
@import '/src/assets/main.css';

#en {
  display: none;
}

.section {
  padding: 0rem 1rem 2rem 1rem; /*top right bottom left*/
}

.page {
  display: flex;
  flex-direction: column;
}

/*red horiz lines*/
hr {
  display: block;
  height: 1px;
  border: 0;
  border-top: 1px solid var(--accent-color);
  margin: 0rem 0.5rem;
  padding: 0;
}

.hr-desktop {
  display: none;
}

.header-mobile {
  display: flex;
  flex-direction: column;
}

.sidebar-desktop {
  display: none;
}

.mobile-section-header {
  display: flex;
  flex-direction: row;
  text-align: left;
  color: var(--accent-color);
  background-color: var(--background-color);
  padding: 0.5rem 0rem;
  margin: 0rem 0.5rem;
  width: 100%;
  /* top: 0;
  position: sticky;
  position: -webkit-sticky; */
}

h2 {
  width: 100%;
  border-bottom: 1px solid var(--accent-color);
  line-height: 0.1rem;
  margin: 0rem 2rem 0rem 0rem;
}

h2 span {
  background: var(--background-color);
  padding: 0rem 1rem 0rem 0rem; /*space between h2 and line*/
}

@media only screen and (min-width: 768px) {
  .header-mobile,
  .footer-mobile {
    display: none;
  }

  .sidebar-desktop {
    display: inline;
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

  hr {
    margin: 0rem 1rem 2rem 1rem;
  }

  .hr-desktop {
    display: block;
  }

  .mobile-section-header {
    display: none;
  }
}

/* .container:hover {
  background-color: var(--hover-color);
} */
</style>
