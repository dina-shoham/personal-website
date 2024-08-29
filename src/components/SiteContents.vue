<script setup>
defineProps({
  items: { type: Array, required: true },
  value: { type: Boolean, required: true }
})
</script>

<template>
  <div :class="`#${value ? 'current-section' : ''}`">
    <!-- eslint-disable-next-line vue/require-v-for-key -->
    <li class="content-li" v-for="item in items">
      <a :href="`#${item.id}`">
        <h2 class="content-item">{{ item.text }}</h2>
      </a>
    </li>
  </div>
  <p v-if="value">value is true</p>
</template>

<style>
.content-item:hover {
  font-weight: 700;
}

/* .current-section {
  background-color: aqua;
  border: 1em;
  border-color: black;
} */

.content-li {
  list-style-type: none;
  text-align: right;
}
</style>
