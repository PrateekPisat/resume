<template>
  <div class="container lg:mx-auto px-4">
    <Header name="PRATEEK PISAT" address="Boston, MA 02120" emailId="pisat.p@northeastern.edu" githubURL="https://www.github.com/PrateekPisat" phoneNumber="781-605-8640" linkedInURL="https://www.linkedin.com/in/prateekpisat" />
    <Education />
    <TechinicalKnowledge />
    <WorkExperience />
    <AcademicProjects />
  </div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import Header from './components/Header.vue';
import Education from './components/Education.vue';
import TechinicalKnowledge from './components/TechinicalKnowledge.vue';
import WorkExperience from './components/WorkExperience.vue'
import AcademicProjects from './components/AcademicProjects.vue'

@Options({components: {Header, Education, TechinicalKnowledge, WorkExperience, AcademicProjects}})
export default class App extends Vue {}
</script>
