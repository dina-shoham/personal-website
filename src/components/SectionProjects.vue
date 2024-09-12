<script setup>
import BubbleItem from './BubbleItem.vue'

defineProps({
  isFrench: { type: Boolean, required: true }
})
</script>

<template>
  <div class="container">
    <div class="project">
      <div class="project-col">
        <img class="project-img" src="/src/assets/le-wordle.png" />
      </div>
      <div class="project-col">
        <h3>Le Wordle</h3>
        <p v-show="!isFrench">
          A French language Wordle clone I built for the children I looked after when I worked as an
          au pair.
        </p>
        <p v-show="isFrench">
          Une version du Wordle du New York Times que j'ai crée pour mes enfants d'accueuil quand
          j'ai travaillé comme jeune fille au pair.
        </p>
        <BubbleItem text="JavaScript" />
        <BubbleItem text="React" />
        <p v-show="!isFrench">
          Check out the source code on
          <a href="https://github.com/dina-shoham/le-wordle" target="_blank">Github</a>, or try it
          out <a href="https://shoham.ca/dina/le-wordle/" target="_blank">here</a>.
        </p>
        <p v-show="isFrench">
          Trouver le code sur
          <a href="https://github.com/dina-shoham/le-wordle" target="_blank">Github</a>, ou
          essayez-le <a href="https://shoham.ca/dina/le-wordle/" target="_blank">ici</a>.
        </p>
      </div>
    </div>
    <div class="project">
      <div class="project-col">
        <img class="project-img" src="/src/assets/portfolio.png" />
      </div>
      <div class="project-col">
        <h3 v-show="!isFrench">Personal Website</h3>
        <h3 v-show="isFrench">Site Personnel</h3>

        <p v-show="!isFrench">A simple and (relatively) static personal portfolio website.</p>
        <p v-show="isFrench">Un site portfolio simple.</p>

        <BubbleItem text="JavaScript" />
        <BubbleItem text="Vue" />

        <p v-show="!isFrench">
          You're visiting it right now! You can also check out the source code on
          <a href="https://github.com/dina-shoham/personal-website" target="_blank">Github</a>.
        </p>
        <p v-show="isFrench">
          Vous y êtes maintenant ! Vous pouvez également trouver le code sur
          <a href="https://github.com/dina-shoham/personal-website" target="_blank">Github</a>.
        </p>
      </div>
    </div>
    <div class="project">
      <div class="project-col">
        <img class="project-img" src="/src/assets/art-gallery.png" />
      </div>
      <div class="project-col">
        <h3 v-show="!isFrench">Art Gallery Application</h3>
        <h3 v-show="isFrench">Application Pour Une Galerie d'Art</h3>
        <p v-show="!isFrench">
          Full-stack application for an art gallery selling artwork, built in a group project for
          ECSE 321 at McGill.
        </p>
        <p v-show="isFrench">
          Application full-stack pour une galerie d'art, développé pour un projet de groupe pour
          ECSE 321 à McGill.
        </p>
        <BubbleItem text="Vue" />
        <BubbleItem text="JavaScript" />
        <BubbleItem text="Java" />
        <BubbleItem text="Gradle" />
        <BubbleItem text="Spring" />
        <BubbleItem text="JUnit" />
        <BubbleItem text="Figma" />
        <p v-show="!isFrench">
          The source code is on
          <a href="https://github.com/McGill-ECSE321-Fall2020/project-group-16" target="_blank"
            >Github</a
          >.
        </p>
        <p v-show="isFrench">
          Le code est sur
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
  flex-direction: column;
}

@media only screen and (min-width: 992px) {
  .project {
    flex-direction: row;
  }
}
</style>
