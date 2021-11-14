<template>
  <div class="container lg:mx-auto px-4">
    <Header name="PRATEEK PISAT" address="Boston, MA 02120" emailId="pisat.p@northeastern.edu" githubURL="www.github.com/PrateekPisat" phoneNumber="781-605-8640" linkedInURL="www.linkedin.com/in/prateekpisat" />
    <Education />
  </div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import Header from './components/Header.vue';
import Education from './components/Education.vue';

@Options({components: {Header, Education}})
export default class App extends Vue {}
</script>
