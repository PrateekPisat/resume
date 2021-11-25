<template>
    <p class="text-2xl font-bold">Academic Projects</p>
    <hr class="border-black text-center text-2xl" data-hr-content="" style="--bg:white; --p:0 10px; --trans-x:-50%; --trans-y:-50%;" />
    <WorkExperienceEntry v-for="entry in workExperienceDetails" :key="entry.title" :title="entry.title" :companyName="entry.companyName" :address="entry.address" :duration="entry.duration" :details="entry.details" />
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import WorkExperienceEntry from './WorkExperienceEntry.vue'

@Options({components: {WorkExperienceEntry}})
export default class AcademicProjects extends Vue {
    get workExperienceDetails(){
        return [
            {
                "title": "Splitwise++",
                "companyName": "Northeastern University",
                "address": "Boston, Massachusetts",
                "duration": "August 2018",
                "details": [
                    "Developed an improved version of a popular app, Splitwise, in a period of 3 weeks using Java and MySQL.",
                    "Rectified major bugs/errors regarding balance calculations and transaction participation within Splitwise.",
                    "Improved overall app reliability, usability, and performance.",

                ],
            },
            {
                "title": "Capture the Campus",
                "companyName": "Northeastern University",
                "address": "Boston, Massachusetts",
                "duration": "April 2018",
                "details": [
                    "Led a team of 4 to design a capture-the-flag web game, in 2 weeks using ReactJS and Elixir.",
                    "Developed a solid understanding of location tracing using HTML5 Geolocation, balanced match-making for multiplayer",
                    "games, designing a responsive UI, and handling API calls to remote services.",
                ],
            }
        ]
    }
}
</script>