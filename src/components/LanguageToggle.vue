<script setup>
const lang = defineModel()

var frenchSelected = false
var englishSelected = true

function setIsFrench(bool) {
  lang.value = bool
  frenchSelected = bool
  englishSelected = !bool
}
</script>

<template>
  <div class="language-toggle">
    <a
      v-bind:style="{
        color: englishSelected ? 'var(--accent-color)' : 'black',
        fontWeight: englishSelected ? '700' : '400'
      }"
      @click="setIsFrench(false)"
      >EN</a
    >
    <span> | </span>
    <a
      v-bind:style="{
        color: frenchSelected ? 'var(--accent-color)' : 'black',
        fontWeight: frenchSelected ? '700' : '400'
      }"
      @click="setIsFrench(true)"
      >FR</a
    >
  </div>
</template>

<style scoped>
@import '/src/assets/main.css';
a {
  font-weight: 400;
  cursor: pointer;
}

.language-toggle {
  text-align: center;
}

/* .is-selected {
  border: 2px solid green;
  color: var(--accent-color);
  font-weight: 700;
}

.not-selected {
  border: 2px solid red;
  color: var(--main-color);
  font-weight: 400;
} */

@media only screen and (min-width: 768px) {
  .language-toggle {
    text-align: right;
  }
}
</style>
