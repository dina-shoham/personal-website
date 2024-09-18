<script setup>
import Bubble from './BubbleItem.vue'

defineProps({
  isFrench: { type: Boolean, required: true }
})
</script>

<template>
  <div class="container">
    <ul v-show="!isFrench" class="timeline">
      <li class="event" data-date="May - Aug 2022">
        <p>
          <b>Software Development Intern</b>,
          <a href="https://www.nuance.com/index.html" target="_blank"
            >Nuance Communications
            <img src="/src/assets/arrow-black.png" />
            <img src="/src/assets/arrow-red.png" />
          </a>
        </p>
        <p>
          Developed a web application to generate requests to Nuance’s NLP API, allowing team
          members and non-technical users alike to easily test the functionality of Nuance’s Web API
          Gateway in the browser.
        </p>
        <Bubble text="React"></Bubble>
        <Bubble text="TypeScript"></Bubble>
        <Bubble text="gRPC-Web"></Bubble>
      </li>

      <li class="event" data-date="May - Aug 2021">
        <p>
          <b>Junior Software Development Intern</b>,
          <a href="https://www.arolytics.com/" target="_blank"
            >Arolytics
            <img src="/src/assets/arrow-black.png" />
            <img src="/src/assets/arrow-red.png" />
          </a>
        </p>
        <p>
          Built, tested, updated, and debugged frontend components for Arolytic’s AROviz emissions
          management software.
        </p>
        <Bubble text="React"></Bubble>
        <Bubble text="JavaScript"></Bubble>
        <Bubble text="Jest"></Bubble>
        <Bubble text="React Testing Library"></Bubble>
        <p>
          Implemented a shell script that generated consulting reports for clients from existing
          emissions modelling code, therefore eliminating hours of work by automating what had been
          a manual process.
        </p>
        <Bubble text="Bash"></Bubble>
        <Bubble text="HTML"></Bubble>
        <Bubble text="R"></Bubble>
        <Bubble text="R Markdown"></Bubble>
      </li>

      <li class="event" data-date="May - Aug 2019">
        <p>
          <b>Research Intern</b>,
          <a href="https://schulich.ucalgary.ca/electrical-software" target="_blank"
            >University of Calgary Department of Software Engineering
            <img src="/src/assets/arrow-black.png" />
            <img src="/src/assets/arrow-red.png" />
          </a>
        </p>
        <p>
          Researched, wrote, and presented a peer-reviewed academic paper on project-based learning
          in software engineering, which was published in the proceedings of the 16th International
          International Conceive-Design-Implement-Operate (CDIO) Conference (check it out
          <a
            href="http://www.cdio.org/knowledge-library/documents/student-perceptions-project-based-learning-software-engineering-course"
            target="_blank"
            ><u>here</u> </a
          >).
        </p>
        <Bubble text="SPSS"></Bubble>
        <Bubble text="LaTeX"></Bubble>
      </li>
    </ul>

    <ul class="timeline" v-show="isFrench">
      <li class="event" data-date="Mai - Août 2022">
        <p>
          <b>Stagiaire Développeur Logiciel</b>,
          <a href="https://www.nuance.com/index.html" target="_blank"
            >Nuance Communications
            <img src="/src/assets/arrow-black.png" />
            <img src="/src/assets/arrow-red.png" />
          </a>
        </p>
        <p>
          Développement d’une application web pour créer des requêtes à l’API de Nuance, permettant
          des membres de l’équipe et des utilisateurs non-techniques de tester facilement le
          fonctionnement du Web API Gateway dans le navigateur.
        </p>
        <Bubble text="React"></Bubble>
        <Bubble text="TypeScript"></Bubble>
        <Bubble text="gRPC-Web"></Bubble>
      </li>

      <li class="event" data-date="Mai - Août 2021">
        <p>
          <b>Stagiaire Développeur Logiciel Junior</b>,
          <a href="https://www.arolytics.com/" target="_blank"
            >Arolytics
            <img src="/src/assets/arrow-black.png" />
            <img src="/src/assets/arrow-red.png" />
          </a>
        </p>
        <p>
          Création, actualisation, débogage, et rédaction de tests pour les composants du frontend
          d’AROviz, le logiciel de gestion des émissions d’Arolytics.
        </p>
        <Bubble text="React"></Bubble>
        <Bubble text="JavaScript"></Bubble>
        <Bubble text="Jest"></Bubble>
        <Bubble text="React Testing Library"></Bubble>
        <p>
          Développement d’un script shell pour générer des rapports de consultation pour des clients
          en utilisant du code pour la modélisation des emissions et du texte pré-écrit, économisant
          ainsi de nombreuses heures du travail en automisant ce processus.
        </p>
        <Bubble text="Bash"></Bubble>
        <Bubble text="HTML"></Bubble>
        <Bubble text="R"></Bubble>
        <Bubble text="R Markdown"></Bubble>
      </li>

      <li class="event" data-date="Mai - Août 2019">
        <p>
          <b>Stagiaire de Recherche</b>,
          <a href="https://schulich.ucalgary.ca/electrical-software" target="_blank"
            >Université de Calgary, Département d’Ingénierie
            <img src="/src/assets/arrow-black.png" />
            <img src="/src/assets/arrow-red.png" />
          </a>
        </p>
        <p>
          Recherche, rédaction, et présentation d’un document de recherche revu par des pairs à
          propos des méthodes d’apprentissage dans le contexte d’ingénierie logicielle, publié dans
          les actes de congrès de la 16ème International CDIO Conference (Conférence internationale
          de “Imaginer-Concevoir-Réaliser-Exploiter”) (lis-le
          <a
            href="http://www.cdio.org/knowledge-library/documents/student-perceptions-project-based-learning-software-engineering-course"
            target="_blank"
            ><u>ici</u> </a
          >).
        </p>
        <Bubble text="SPSS"></Bubble>
        <Bubble text="LaTeX"></Bubble>
      </li>
    </ul>

    <p v-show="!isFrench">
      Download my full CV in
      <a
        href="https://github.com/dina-shoham/cv/blob/main/dina_shoham_cv_english.pdf"
        target="_blank"
        ><u>English</u></a
      >
      or
      <a
        href="https://github.com/dina-shoham/cv/blob/main/dina_shoham_cv_francais.pdf"
        target="_blank"
        ><u>French</u></a
      >.
    </p>

    <p v-show="isFrench">
      Téléchargez mon CV en
      <a
        href="https://github.com/dina-shoham/cv/blob/main/dina_shoham_cv_francais.pdf"
        target="_blank"
        ><u>français</u></a
      >
      ou en
      <a
        href="https://github.com/dina-shoham/cv/blob/main/dina_shoham_cv_english.pdf"
        target="_blank"
        ><u>anglais</u></a
      >
      .
    </p>
  </div>
</template>

<style scoped>
@import '/src/assets/main.css';

a {
  font-weight: 400;
  /* text-decoration: underline; */
}

img {
  height: 0.8rem;
  width: 0.8rem;
  margin: 0rem;
  padding: 0rem;
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

/*Adapted from https://codepen.io/samerpik/embed/OVKyVZ? */
.timeline {
  left: 8rem;
  border-left: 2px solid var(--accent-color);
  position: relative;
  padding: 0rem 8rem 0rem 1rem;
  list-style: none;
  text-align: left;
  width: (100% - 8rem);
}

.timeline .event {
  position: relative;
}

.timeline .event:last-of-type {
  padding-bottom: 0;
  margin-bottom: 0;
  border: none;
}

.timeline .event:before,
.timeline .event:after {
  position: absolute;
  display: block;
  top: 0;
}

/*date*/
.timeline .event:before {
  left: -10rem;
  /* color: #000; */
  content: attr(data-date);
  text-align: right;
  font-size: 14px;
  font-style: italic;
  min-width: 120px;
}

/*dots*/
.timeline .event:after {
  left: -1.3rem;
  background: var(--accent-color);
  border-radius: 50%;
  height: 0.5rem;
  width: 0.5rem;
  content: '';
  top: 0.3rem;
}

@media only screen and (min-width: 768px) {
  .timeline {
    left: 8rem;
    padding: 0rem 8rem 0rem 1rem;
  }
}
</style>
