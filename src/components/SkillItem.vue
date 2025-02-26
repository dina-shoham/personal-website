<script setup>
defineProps({
  text: { type: String, required: true }
})
</script>

<template>
    <span class="skill-item">{{text}}</span>
</template>