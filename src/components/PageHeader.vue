<script setup>
import Links from './ContactIcons.vue'
defineProps({
  name: { type: String, required: true },
  title: { type: String, required: true }
})
</script>

<template>
  <div class="header">
    <h1>{{ name }}</h1>
    <h2>{{ title }}</h2>
    <br />
    <Links></Links>
  </div>
</template>

<style scoped>
h1,
h2 {
  text-align: right;
  line-height: normal;
  margin: 0;
}

.header {
  /* margin: 1rem; */
  float: right;
  margin: 0rem 0rem 5rem 0rem;
}
</style>
