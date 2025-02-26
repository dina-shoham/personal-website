<script setup>
defineProps({
  text: { type: String, required: true },
  link: { type: String, required: true }
})
</script>

<template>
    <a class="skill-item" :href="`${link}`" target="_blank">{{text}}</a>
</template>