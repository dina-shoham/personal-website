<script setup>
import Bubble from './BubbleItem.vue'
</script>

<template>
  <div class="container">
    <ul class="timeline">
      <li class="event" data-date="May - Aug 2022">
        <p>
          <b>Software Development Intern</b>,
          <a href="https://www.nuance.com/index.html" target="_blank"
            >Nuance Communications
            <img src="../assets/arrow-black.png" />
            <img src="../assets/arrow-red.png" />
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
            <img src="../assets/arrow-black.png" />
            <img src="../assets/arrow-red.png" />
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
            <img src="../assets/arrow-black.png" />
            <img src="../assets/arrow-red.png" />
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
    <p>
      Download my full CV in
      <a href="../../public/dina_shoham_cv_f2024_english.pdf" target="_blank" :download>English</a>
      or
      <a href="../../public/dina_shoham_cv_f2024_francais.pdf" target="_blank" :download>French</a>.
    </p>
  </div>
</template>

<style scoped>
@import '../assets/main.css';

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
</style>
