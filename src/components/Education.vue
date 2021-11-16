<template>
  <div>
    <p class="text-2xl font-bold">Education</p>
    <hr class="border-black text-center text-2xl" data-hr-content="" style="--bg:white; --p:0 10px; --trans-x:-50%; --trans-y:-50%;" />
    <EducationEntry university="Northerastern University" address="Boston, MA" college="College of Computer and Information Science" degreeName="Master’s Degree in Computer Science" graduationDate="December 2019" gpa=3.66 />
    <br>
    <EducationEntry university="Mumbai University" address="Mumbai, India" college="" degreeName="Bachelor’s Degree in Computer Engineering" graduationDate="June 2017" gpa=3.25 />
    <br>
  </div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import EducationEntry from './EducationEntry.vue';

@Options({
  components: {
    EducationEntry
  }
})
export default class Education extends Vue {
  
}
</script>