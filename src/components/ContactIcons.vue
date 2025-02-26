<script setup></script>

<template>
  <div class="icons">
    <a href="mailto:dina.shoham@gmail.com">
      <img src="/src/assets/email.png" alt="Black mail icon"/>
      <img src="/src/assets/email-red.png" alt="Red mail icon"/>
    </a>
    <a href="https://linkedin.com/in/dina-shoham" target="_blank">
      <img src="/src/assets/linkedin.png" alt="Black LinkedIn icon"/>
      <img src="/src/assets/linkedin-red.png" alt="Red LinkedIn icon"/>
    </a>
    <a href="https://github.com/dina-shoham" target="_blank">
      <img src="/src/assets/github.png" alt="Black GitHub icon"/>
      <img src="/src/assets/github-red.png" alt="Red GitHub icon"/>
    </a>
  </div>
</template>

<style>
.icons {
  display: flex;
  justify-content: left;
}

a img:last-child {
  display: none;
}
a:hover img:last-child {
  display: inline;
}
a:hover img:first-child {
  display: none;
}

img {
  width: 1.5rem;
  height: 1.5rem;
  margin: 1rem 0.5rem 1rem 0.5rem;
}
</style>
