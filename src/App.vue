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
    <div class="header-mobile">
      <div>
        <Header name="Dina Shoham" title="Software Engineer"></Header>
      </div>
      <hr class="hr-desktop" />
    </div>
    <div class="sidebar-desktop">
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
        <div class="mobile-section-header">
          <h2><span>About</span></h2>
        </div>
        <SectionAbout></SectionAbout>
      </div>
      <hr class="hr-desktop" />
      <div class="section" id="experience">
        <div class="mobile-section-header">
          <h2><span>Experience</span></h2>
        </div>
        <SectionExperience></SectionExperience>
      </div>
      <hr class="hr-desktop" />
      <div class="section" id="skills">
        <div class="mobile-section-header">
          <h2><span>Skills</span></h2>
        </div>
        <SectionSkills></SectionSkills>
      </div>
      <hr class="hr-desktop" />
      <div class="section" id="projects">
        <div class="mobile-section-header">
          <h2><span>Projects</span></h2>
        </div>
        <SectionProjects></SectionProjects>
      </div>
    </div>
  </div>
</template>

<style scoped>
@import '/src/assets/main.css';

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
  z-index: 1;
  width: 100%;
  position: sticky;
  top: 0;
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
  .header-mobile {
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
