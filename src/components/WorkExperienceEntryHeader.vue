<template>
    <div>
        <div class="inline-block float-left">
            <span class="font-bold">{{ title }} </span>
        </div>
        <div class="inline-block float-right">{{ duration }}</div>
        <br>
        <div>{{ companyName }}, {{ address }}</div>
    </div>
</template>
<script lang="ts">
import { Vue } from 'vue-class-component';
import { Prop } from 'vue-property-decorator';

export default class WorkExperienceEntryHeader extends Vue {
    @Prop() title!: string;
    @Prop() companyName !: string;
    @Prop() address !: string;
    @Prop() duration !: string;
    @Prop() details!: string[];
}
</script>