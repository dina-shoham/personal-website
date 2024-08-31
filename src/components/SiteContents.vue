<script setup>
defineProps({
  items: { type: Array, required: true },
  value: { type: Boolean, required: true }
})
</script>

<script>
function setCurrentSection(section) {
  switch (section) {
    case 'About':
      document.getElementById('About').style.color = '#b4270d'
      document.getElementById('Skills').style.color = '#000'
      document.getElementById('Experience').style.color = '#000'
      document.getElementById('Projects').style.color = '#000'
      break
    case 'Skills':
      document.getElementById('About').style.color = '#000'
      document.getElementById('Skills').style.color = '#b4270d'
      document.getElementById('Experience').style.color = '#000'
      document.getElementById('Projects').style.color = '#000'
      break
    case 'Experience':
      document.getElementById('About').style.color = '#000'
      document.getElementById('Skills').style.color = '#000'
      document.getElementById('Experience').style.color = '#b4270d'
      document.getElementById('Projects').style.color = '#000'
      break
    case 'Projects':
      document.getElementById('About').style.color = '#000'
      document.getElementById('Skills').style.color = '#000'
      document.getElementById('Experience').style.color = '#000'
      document.getElementById('Projects').style.color = '#b4270d'
      break
  }
  console.log('here')
}
</script>

<template>
  <div>
    <!-- eslint-disable-next-line vue/require-v-for-key -->
    <li class="content-li" v-for="item in items">
      <a :id="`${item.text}`" :href="`#${item.id}`" @click="setCurrentSection(item.text)">
        <h2 class="content-item">{{ item.text }}</h2>
      </a>
    </li>
  </div>
</template>

<style>
@import '../assets/main.css';

.content-li {
  list-style-type: none;
  text-align: right;
}
</style>
