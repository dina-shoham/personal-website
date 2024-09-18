<script setup>
import { onMounted } from 'vue'

const lang = defineModel()

function styleLanguages(isFrench) {
  console.log('styler')
  if (isFrench) {
    console.log('is french')
    console.log(document.getElementById('en-button'))
    console.log(document.getElementById('fr-button'))
    document.getElementById('en-button').style.fontWeight = '400'
    document.getElementById('en-button').style.color = '#000'
    document.getElementById('fr-button').style.fontWeight = '700'
    document.getElementById('fr-button').style.color = '#b4270d'
  } else {
    console.log('is english')
    console.log(document.getElementById('en-button'))
    console.log(document.getElementById('fr-button'))
    document.getElementById('en-button').style.fontWeight = '700'
    document.getElementById('en-button').style.color = '#b4270d'
    document.getElementById('fr-button').style.fontWeight = '400'
    document.getElementById('fr-button').style.color = '#000'
  }
}

function setIsFrench(bool) {
  console.log('setter')
  lang.value = bool
  styleLanguages(bool)
}

onMounted(() => {
  styleLanguages(lang.value)
})
</script>

<template>
  <div class="language-toggle">
    <a id="en-button" @click="setIsFrench(false)">EN</a>
    <span> | </span>
    <a id="fr-button" @click="setIsFrench(true)">FR</a>
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
