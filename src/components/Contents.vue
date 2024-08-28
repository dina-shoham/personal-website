<script setup>
defineProps({
  items: { type: Array, required: true }
})
</script>

<template>
  <li class="content-li" v-for="item in items">
    <a :href="`#${item.id}`"
      ><h2 class="content-item">{{ item.text }}</h2></a
    >
  </li>
</template>

<style>
.content-item:hover {
  font-weight: 700;
}

.content-li {
  list-style-type: none;
  text-align: right;
}
</style>
