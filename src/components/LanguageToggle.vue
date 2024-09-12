<script setup>
import { onMounted } from 'vue'

const lang = defineModel()

function styleLanguages(isFrench) {
  if (isFrench) {
    document.getElementById('en').style.fontWeight = '400'
    document.getElementById('en').style.color = '#000'
    document.getElementById('fr').style.fontWeight = '700'
    document.getElementById('fr').style.color = '#b4270d'
  } else {
    document.getElementById('en').style.fontWeight = '700'
    document.getElementById('en').style.color = '#b4270d'
    document.getElementById('fr').style.fontWeight = '400'
    document.getElementById('fr').style.color = '#000'
  }
}

function setIsFrench(bool) {
  lang.value = bool
  styleLanguages(bool)
}

onMounted(() => {
  styleLanguages(lang.value)
})
</script>

<template>
  <div class="language-toggle">
    <a id="en" @click="setIsFrench(false)">EN</a>
    <span> | </span>
    <a id="fr" @click="setIsFrench(true)">FR</a>
  </div>
</template>

<style>
@import '/src/assets/main.css';
a {
  font-weight: 400;
  cursor: pointer;
}

.language-toggle {
  text-align: center;
}

@media only screen and (min-width: 768px) {
  .language-toggle {
    text-align: right;
  }
}
</style>
