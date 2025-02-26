<script setup lang="ts">
import SkillItem from './SkillItem.vue';

</script>

<template>
  <div class="section">
    <div class="section-head">
        <h3>Projects</h3>
    </div>
    <div class="section-body">
      <div class="project">
        <div class="project-head">
          <p>Le Wordle</p>
          <img class="project-img" src="/src/assets/wordle-mockup.png" alt="Mockup of a Wordle application"/>
        </div>
        <div class="project-body">
          <p>A French language Wordle clone I built for the children I looked after when I worked as an au pair.</p>
          <p>Try it out <a href="https://shoham.ca/dina/le-wordle/" target="_blank">here</a> or check out the source code on <a href="https://github.com/dina-shoham/le-wordle" target="_blank">Github</a>.</p>
          <SkillItem text="JavaScript"></SkillItem>
          <SkillItem text="React"></SkillItem>
        </div>
      </div>

      <div class="project">
        <div class="project-head">
          <p>Personal Website</p>
          <img class="project-img" src="/src/assets/portfolio-mockup.png" alt="Mockup of a simple personal website"/>
        </div>
        <div class="project-body">
          <p>A simple static personal portfolio website.</p>
          <p>You're visiting the current version here, but see previous iterations on different branches on <a href="https://github.com/dina-shoham/personal-website" target="_blank">Github</a>.</p>
          <SkillItem text="JavaScript"></SkillItem>
          <SkillItem text="Vue.js"></SkillItem>
        </div>
      </div>
    </div>
  </div>
</template>

<style>
.project-img {
  width: 18rem;
  height: 12rem;
  margin: -1.5rem 0rem 0rem -1.5rem;
}

.project {
  display: flex;
  flex-direction: row;
}

.project-body {
  margin: 2rem 0rem 0rem 0rem;
}
</style>