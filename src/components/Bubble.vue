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
button {
  padding: 0.4rem 1rem;
  margin: 0rem 0.5rem 1rem 0rem;
  border-radius: 0.75rem;
  border: none;
  text-align: center;
  font-size: 12px;
  font-weight: 600;
}

.grey {
  background-color: rgb(234, 230, 228);
}

.green {
  background-color: rgb(185, 229, 174);
}

.yellow {
  background-color: rgb(255, 234, 167);
}
</style>
