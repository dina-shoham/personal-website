<script setup>
defineProps({
  isFrench: { type: Boolean, required: true }
})
</script>

<template>
  <div class="container">
    <p v-show="!isFrench">
      Hi, I'm Dina! I'm a recent software engineering graduate from McGill University. I've just
      returned to Canada after a year abroad in Versailles, France, where I was studying the
      language and working as an au pair.
    </p>
    <p v-show="!isFrench">
      I am currently seeking software development or software engineering opportunities beginning in
      fall 2024. I am eager to leverage my industry experience in front-end development, the
      programming and interpersonal skills I developed through my studies, and an enthusiasm for new
      and challenging experiences that I discovered during my year abroad, as I embark on this next
      chapter.
    </p>
    <p v-show="isFrench">
      Bonjour, je m'appelle Dina ! Je suis une récente diplômée de l’Université McGill. Je viens de
      rentrer au Canada après avoir passé un an à Versailles, France, où j'étudiais la langue
      française et travaillais comme jeune fille au pair.
    </p>
    <p v-show="isFrench">
      Je suis maintenant à la recherche d’un poste en développement logiciel ou ingéniérie
      logicielle à partir de l’automne 2024. Je suis motivée à mettre à profit mon expérience dans
      le développement front-end acquise dans le secteur, mes compétences en programmation et mes
      qualités relationnelles développés pendant mes études, ainsi qu'un enthousiasme pour des
      nouvelles expériences que j'ai découvert pendant mon année en France.
    </p>
  </div>
</template>

<style></style>
