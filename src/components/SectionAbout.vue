<script setup>
defineProps({
  isFrench: { type: Boolean, required: true }
})
</script>

<template>
  <div class="container">
    <p v-show="!isFrench">
      A recent software engineering graduate from McGill University, recently returned to Canada
      after a year abroad in Versailles, France studying the language. Seeking software development
      and software engineering opportunities beginning in fall 2024. Eager to leverage industry
      experience in front-end development and programming and interpersonal skills developed through
      my studies, with the goal of learning new skills, languages, and domains.
    </p>
    <p v-show="isFrench">
      Une récente diplômée de l’Université McGill, je suis à la recherche d’un poste en
      développement logiciel ou ingéniérie logicielle à partir de l’automne 2024. Motivée à mettre à
      profit mon expérience dans le développement front-end acquise dans le secteur, mes compétences
      en programmation et mes qualités relationnelles développés pendant mes études, afin
      d’apprendre de nouvelles compétences, langues et domaines.
    </p>
  </div>
</template>

<style></style>
