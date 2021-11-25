<template>
    <div class="text-justify">
        <WorkExperienceEntryHeader :title="title" :companyName="companyName" :address="address" :duration="duration" />
        <div class="space-x-6" v-for="detail in details" :key=detail>
            <i class="fas fa-circle fa-xs"></i> 
            <span>{{ detail }}</span>
        </div>
        <br>
    </div>
</template>
<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import { Prop } from 'vue-property-decorator';
import WorkExperienceEntryHeader from  './WorkExperienceEntryHeader.vue';

@Options({components: {WorkExperienceEntryHeader}})
export default class WorkExperienceEntry extends Vue {
    @Prop() title!: string;
    @Prop() companyName !: string;
    @Prop() address !: string;
    @Prop() duration !: string;
    @Prop() details!: string[];
}
</script>