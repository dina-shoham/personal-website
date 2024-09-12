<script setup>
import Links from './ContactIcons.vue'
defineProps({
  isFrench: { type: Boolean, required: true }
})
</script>

<template>
  <div class="header">
    <h1>Dina Shoham</h1>
    <h2 v-show="!isFrench">Software Engineer</h2>
    <h2 v-show="isFrench">Ingénieure Logiciel</h2>
    <br />
    <Links></Links>
  </div>
</template>

<style scoped>
.header {
  float: center;
  margin: 0rem 0rem 0rem 1rem;
}

h1,
h2 {
  text-align: center;
  line-height: normal;
  margin: 0;
}

@media only screen and (min-width: 768px) {
  .header {
    width: 100%;
    float: right;
    margin: 0rem 0rem 5rem 0rem;
  }

  h1,
  h2 {
    text-align: right;
  }
}
</style>
