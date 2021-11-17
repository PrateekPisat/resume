<template>
    <p class="text-2xl font-bold">Work Experience</p>
    <hr class="border-black text-center text-2xl" data-hr-content="" style="--bg:white; --p:0 10px; --trans-x:-50%; --trans-y:-50%;" />
    <WorkExperienceEntry v-for="entry in workExperienceDetails" :key="entry.title" :title="entry.title" :companyName="entry.companyName" :address="entry.address" :duration="entry.duration" :details="entry.details" />
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import WorkExperienceEntry from './WorkExperienceEntry.vue'

@Options({components: {WorkExperienceEntry}})
export default class WorkExperience extends Vue {
    get workExperienceDetails(){
        return [
            {
                "title": "Software Engineer",
                "companyName": "Known Global",
                "address": "Boston, Massachusetts",
                "duration": "January 2020 - Present",
                "details": [
                    "Engineered a tool utilizing Python and VueJS, facilitating users to create a batch of ads, across multiple ad platforms,  reducing the amount of time spent in doing the same via the UI.",
                    "Designed data pipelines using Airflow and Spark to aggregate ingest data and performance metrics to an internal database, allowing scientists to analyse it more efficiently.",
                    "Developed a tool employing Python and the Google Sheets API, to automate client report generation; saving time required to aggregate data manually eliminating human errors, and improving accuracy.",
                    "Implemented Airflow DAGs employing Python and Snowflake to ingest app performance metrics and reports leading to effective analysis and improvement in overall sales.",
                    "Optimized inefficient SQL queries leveraging CTEs thereby reducing execution time by 25% on average, improving performance and availability of the service.",
                    "Added a Redis and MongoDB Pytest fixture to an open-source Python library, pytest-mock-resources, eliminating the need to rely on an external database instance for writing unit tests.",
                    "Designed and integrated an asynchronous endpoint into existing API using Python, Celery and PostgreSQL that efficiently filters over 33 million inventory records and returns the results and inventory metrics.",
                    "Contributed to and maintained an open source Python library, htxml, improving the HTML parser, adding support for new tags and addressing active issues.",
                    "Designed efficient queries to analyse over 12 million records in BigQuery and built automated pipelines around it using Python and Airflow.",

                ]
            },
            {
                "title": "Graduate Teaching Assistant",
                "companyName": "Northeastern University",
                "address": "Boston, Massachusetts",
                "duration": "September 2019 - December 2019",
                "details": [
                    "Developed Bash and Python scripts to automatically grade assignments and clone repositories, diminishing manual effort and saving time.",
                    "Conducted office hours; helping students understand core data structures such as stacks, queues, and hash-tables as well as core systems concepts such as memory allocation, compilers, and linkers.",
                ]
            },
            {
                "title": "Software Engineer Co-Op",
                "companyName": "Known Global",
                "address": "Boston, Massachusetts",
                "duration": "January 2019 - August 2019",
                "details": [
                    "Engineered a web application leveraging Django and PostgreSQL to build dynamic dashboards, visualizing the performance of various ad segments across multiple networks, allowing users to process data in a clean and simplified manner.",
                    "Created a lightweight library around Amazon Sagemaker utilizing Python to synchronize remote training and tuning job parameters with a local database, helping users analyze training parameters across multiple jobs faster.",
                    "Designed and implemented a Python tool using Sphinx to auto-generate documentation for a given project and publish it to the organization’s documentation page."
                ]
            }
        ]
    }
}
</script>
