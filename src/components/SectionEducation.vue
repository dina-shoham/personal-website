<script setup>
defineProps({
  isFrench: { type: Boolean, required: true }
})
</script>

<template>
  <div class="container">
    <div v-show="!isFrench">
      <p><b>Bachelor of Software Engineering</b>, McGill University</p>
      <p>Minor in Arts (Philosophy and Art History concentration)</p>
      <p></p>
    </div>
    <p v-show="isFrench"></p>
  </div>
</template>

<style></style>
