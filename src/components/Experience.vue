<script setup lang="js">
  import SkillItem from './SkillItem.vue';
  import SkillItemLink from './SkillItemLink.vue';
</script>

<template>
  <div class="section">
    <div class="section-head">
        <h3>Experience</h3>
    </div>
    <div class="section-body">
      <ul class="timeline">
        
        <!-- ACN -->
        <li class="event">
          <div class="event-date">
            <span>Dec 2024 - present</span>
          </div>
          <div class="event-content">
            <p>Full Stack Analyst</p>
            <p><a href="https://www.accenture.com/" target="_blank">Accenture</a></p>
          </div>
        </li>

        <!-- GAP YR -->
        <li class="event">
          <div class="event-date">
            <span>Aug 2023 - Jul 2024</span>
          </div>
          <div class="event-content">
            <p>Year Abroad</p>
            <p>Versailles, France</p>
            <p></p>
            <SkillItem text="DALF C1 Diploma"></SkillItem>
          </div>
        </li>

        <!-- NUANCE -->
        <li class="event">
          <div class="event-date">
            <span>May - Aug 2022</span>
          </div>
          <div class="event-content">
            <p>Software Development Intern</p>
            <p><a href="https://www.nuance.com/index.html" target="_blank">Nuance Communications</a></p>
            <SkillItem text="React">/</SkillItem>
            <SkillItem text="TypeScript"></SkillItem>
            <SkillItem text="gRPC-Web"></SkillItem>
          </div>
        </li>

        <!-- AROLYTICS -->
        <li class="event">
          <div class="event-date">
            <span>May - Aug 2021</span>
          </div>
          <div class="event-content">
            <p>Junior Software Development Intern</p>
            <p><a href="https://www.arolytics.com/" target="_blank">Arolytics</a></p>
            <SkillItem text="React"></SkillItem>
            <SkillItem text="JavaScript"></SkillItem>
            <SkillItem text="Jest"></SkillItem>
            <SkillItem text="Bash"></SkillItem>
          </div>
        </li>

        <!-- AROLYTICS -->
        <li class="event">
          <div class="event-date">
            <span>May - Aug 2019</span>
          </div>
          <div class="event-content">
            <p>Research Intern</p>
            <p><a href="https://schulich.ucalgary.ca/electrical-software" target="_blank">University of Calgary Dept. of Software Engineering</a></p>
            <SkillItemLink text="Research Paper" link="https://cdio.org/knowledge-library/documents/student-perceptions-project-based-learning-software-engineering-course"></SkillItemLink>
          </div>
        </li>

      </ul>
      <p>View my full CV <a href="https://github.com/dina-shoham/cv/blob/main/dina_shoham_cv_2025_english.pdf" target="_blank">here</a>.</p>
    </div>
  </div>
</template>

<style scoped>
@import '/src/assets/main.css';

.timeline {
  margin: 1rem 0rem 0rem 0rem;
  border-left-style: solid;
  border-left-width: 0.1rem;
  border-left-color: var(--main-color);
}

.event {
  margin: 0rem 0rem 2rem -1.9rem; 
  /* -1.9rem aligns dots onto line */
}

.event-date {
  text-align: right;
  color: var(--secondary-color);
}

.event-content {
  margin: -1.7rem 0rem 0rem 0rem;
}

p {
  margin: 0.5rem 0rem;
}
</style>