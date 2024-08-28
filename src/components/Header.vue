<script setup>
import Links from './Links.vue'
defineProps({
  name: { type: String, required: true },
  title: { type: String, required: true }
})
</script>

<template>
  <div class="header">
    <h1>{{ name }}</h1>
    <h2>{{ title }}</h2>
    <Links></Links>
  </div>
</template>

<style scoped>
h1,
h2 {
  text-align: right;
}

.header {
  float: right;
}
</style>
