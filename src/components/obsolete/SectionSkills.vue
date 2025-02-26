<script setup>
import Bubble from './BubbleItem.vue'

defineProps({
  isFrench: { type: Boolean, required: true }
})
</script>

<template>
  <div class="container">
    <div>
      <h3 v-show="!isFrench">Programming Languages</h3>
      <h3 v-show="isFrench">Langages de programmation</h3>
    </div>
    <div>
      <Bubble text="JavaScript" colour="green"></Bubble>
      <Bubble text="TypeScript" colour="green"></Bubble>
      <Bubble text="Java" colour="green"></Bubble>
      <Bubble text="HTML" colour="green"></Bubble>
      <Bubble text="CSS" colour="green"></Bubble>
    </div>
    <div>
      <Bubble text="Python" colour="yellow"></Bubble>
      <Bubble text="Bash" colour="yellow"></Bubble>
      <Bubble text="C" colour="yellow"></Bubble>
      <Bubble text="SQL" colour="yellow"></Bubble>
    </div>
    <div>
      <h3 v-show="!isFrench">Libraries and Frameworks</h3>
      <h3 v-show="isFrench">Bibliothèques et Frameworks</h3>
    </div>
    <div>
      <Bubble text="React"></Bubble>
      <Bubble text="Node.js"></Bubble>
      <Bubble text="Vue"></Bubble>
      <Bubble text="Jest"></Bubble>
      <Bubble text="Spring"></Bubble>
      <Bubble text="JUnit" colour="grey"></Bubble>
      <Bubble text="Django"></Bubble>
      <Bubble text="Flask"></Bubble>
      <Bubble text="gRPC"></Bubble>
      <Bubble text="PostgreSQL"></Bubble>
    </div>
  </div>
</template>
