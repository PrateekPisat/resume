<template>
    <p class="text-2xl font-bold">Techinical Knowledge</p>
    <hr class="border-black text-center text-2xl" data-hr-content="" style="--bg:white; --p:0 10px; --trans-x:-50%; --trans-y:-50%;" />
    <table class="table-fixed">
        <thead>
            <tr>
                <th class="w-1/6"></th>
                <th class="w-1/2"></th>
            </tr>
        </thead>
        <tbody>
            <TechinicalKnowledgeRow v-for="(detail, header) in details" :key="detail.key" :header="header" :details="detail" />
        </tbody>
    </table>
    <br>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import TechinicalKnowledgeRow from "./TechinicalKnowledgeRow.vue"

@Options({components: {TechinicalKnowledgeRow}})
export default class  extends Vue {
    get details(){
        return {
            "Languages": ["Python (Proficient)", "SQL (Proficient)", "TypeScript (Proficient)", "Java (Prior Knowledge)"],
            "Databases": ["PostgreSQL", "Google BigQuery", "MongoDB", "Snowflake", "AWS Athena", "Redis"],
            "CI/CD":["CircleCI", "Jenkins"],
            "Systems": ["Docker", "Airflow", "Apache Spark", "Linux", "macOS"],
            "Web Technologies": ["NodeJS", "VueJS", "Django", "Flask", "Nginx"]
        }
    }
}
</script>
