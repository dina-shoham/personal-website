<script setup>
defineProps({
  isFrench: { type: Boolean, required: true },
  items: { type: Array, required: true }
})
</script>

<script>
var red = '#b4270d'
var black = '#000'

function setCurrentSection(section) {
  switch (section) {
    case 'about':
      document.getElementById('about-nav').style.color = red
      document.getElementById('skills-nav').style.color = black
      document.getElementById('experience-nav').style.color = black
      document.getElementById('projects-nav').style.color = black
      break
    case 'skills':
      document.getElementById('about-nav').style.color = black
      document.getElementById('skills-nav').style.color = red
      document.getElementById('experience-nav').style.color = black
      document.getElementById('projects-nav').style.color = black
      break
    case 'experience':
      document.getElementById('about-nav').style.color = black
      document.getElementById('skills-nav').style.color = black
      document.getElementById('experience-nav').style.color = red
      document.getElementById('projects-nav').style.color = black
      break
    case 'projects':
      document.getElementById('about-nav').style.color = black
      document.getElementById('skills-nav').style.color = black
      document.getElementById('experience-nav').style.color = black
      document.getElementById('projects-nav').style.color = red
      break
  }
}
</script>

<template>
  <div>
    <!-- eslint-disable-next-line vue/require-v-for-key -->
    <li class="content-li" v-for="item in items">
      <a :id="`${item.id}-nav`" :href="`#${item.id}`" @click="setCurrentSection(item.id)">
        <h2 class="content-item" v-if="!isFrench">{{ item.textEN }}</h2>
        <h2 class="content-item" v-else>{{ item.textFR }}</h2>
        <!-- <h2 class="content-item">{{ !isFrench ? item.textEN : item.textFR }}</h2> -->
      </a>
    </li>
  </div>
</template>

<style>
@import '/src/assets/main.css';

.content-li {
  list-style-type: none;
  text-align: right;
}
</style>
