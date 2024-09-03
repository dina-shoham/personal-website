<script setup></script>

<template>
  <div class="icons">
    <a href="mailto:dina.shoham@gmail.com">
      <img src="/src/assets/email.png" />
      <img src="/src/assets/email-red.png" />
    </a>
    <a href="https://linkedin.com/in/dina-shoham" target="_blank">
      <img src="/src/assets/linkedin.png" />
      <img src="/src/assets/linkedin-red.png" />
    </a>
    <a href="https://github.com/dina-shoham" target="_blank">
      <img src="/src/assets/github.png" />
      <img src="/src/assets/github-red.png" />
    </a>
  </div>
</template>

<style>
.icons {
  display: flex;
  justify-content: center;
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

@media only screen and (min-width: 768px) {
  .icons {
    float: right;
  }
}

img {
  width: 1.5rem;
  height: 1.5rem;
  margin: 0rem 0.5rem 1rem 0.5rem;
}
</style>
