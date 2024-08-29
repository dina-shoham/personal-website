<script setup>
import Bubble from './BubbleItem.vue'
</script>

<template>
  <div class="container">
    <div>
      <h3>Programming Languages</h3>
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
      <h3>Libraries and Frameworks</h3>
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
