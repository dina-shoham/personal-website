<script setup>
defineProps({
  text: { type: String, required: true },
  colour: { type: String }
})
</script>

<template>
  <button v-bind:class="colour">{{ text }}</button>
</template>

<style scoped>
@import '/src/assets/main.css';

button {
  -webkit-appearance: none;
  -moz-appearance: none;
  appearance: none;
  color: black !important;
  background-color: var(--bubble-color);
  padding: 0.4rem 1rem;
  margin: 0rem 0.5rem 1rem 0rem;
  border-radius: 0.75rem;
  border: none;
  text-align: center;
  font-size: 12px;
  font-weight: 600;
}

.green {
  color: black;
  background-color: rgb(185, 229, 174);
}

.yellow {
  color: black;
  background-color: rgb(255, 234, 167);
}
</style>
