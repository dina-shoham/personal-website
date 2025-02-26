<script setup>
import Header from './components/Header.vue'
import Experience from './components/Experience.vue';
import Projects from './components/Projects.vue';
import Contact from './components/Contact.vue';

console.log(window.navigator.language)
</script>

<template>
  <div class="page">
    <div id="header">
      <Header></Header>
    </div>
    
    <div id="experience">
      <Experience></Experience>
    </div>

    <div id="projects">
      <Projects></Projects>
    </div>

    <div id="contact">
      <Contact></Contact>
    </div>

  </div>
</template>

<style scoped>
@import '/src/assets/main.css';

@media only screen and (min-width: 768px) {
  /* disable mobile */
}
</style>
