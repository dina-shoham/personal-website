<script setup>
import BubbleItem from './BubbleItem.vue'
</script>

<template>
  <div class="container">
    <div class="project">
      <div class="project-col">
        <img class="project-img" src="/src/assets/le-wordle.png" />
      </div>
      <div class="project-col">
        <h3>Le Wordle</h3>
        <p>
          A French language Wordle clone I built for the children I looked after when I worked as an
          au pair.
        </p>
        <BubbleItem text="JavaScript" />
        <BubbleItem text="React" />
        <p>
          Check out the source code on
          <a href="https://github.com/dina-shoham/le-wordle" target="_blank">Github</a>, or try it
          out <a href="https://shoham.ca/dina/le-wordle/" target="_blank">here</a>.
        </p>
      </div>
    </div>
    <div class="project">
      <div class="project-col">
        <img class="project-img" src="/src/assets/portfolio.png" />
      </div>
      <div class="project-col">
        <h3>Personal Website</h3>
        <p>A simple and (relatively) static personal portfolio website.</p>
        <BubbleItem text="JavaScript" />
        <BubbleItem text="Vue" />
        <p>
          You're visiting it right now! You can also check out the source code on
          <a href="https://github.com/dina-shoham/personal-website" target="_blank">Github</a>.
        </p>
      </div>
    </div>
    <div class="project">
      <div class="project-col">
        <img class="project-img" src="/src/assets/art-gallery.png" />
      </div>
      <div class="project-col">
        <h3>Art Gallery Website</h3>
        <p>
          Full-stack application for an art gallery selling artwork, built in a group project for
          ECSE 321 at McGill.
        </p>
        <BubbleItem text="Vue" />
        <BubbleItem text="JavaScript" />
        <BubbleItem text="Java" />
        <BubbleItem text="Gradle" />
        <BubbleItem text="Spring" />
        <BubbleItem text="JUnit" />
        <BubbleItem text="Figma" />
        <p>
          The source code is on
          <a href="https://github.com/McGill-ECSE321-Fall2020/project-group-16" target="_blank"
            >Github</a
          >.
        </p>
      </div>
    </div>
  </div>
</template>

<style>
.project {
  padding: 0rem 0rem 2rem 0rem;
}

.project-img {
  width: 15rem;
  height: 10rem;
  padding: 0.5rem 2rem 0rem 0rem;
}

.project {
  display: flex;
  flex-direction: row;
}
</style>
