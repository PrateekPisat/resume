<template>
    <div>
        <div class="inline-block float-left">
            <span class="font-bold">{{ university }}, </span>
            <span>{{ address }}</span>
        </div>
        <div class="inline-block float-right">{{ graduationDate }}</div>
        <br>
        <div>{{ college }}</div>
        <div>
            <span class="italic">{{ degreeName }}</span>
            <span>, GPA: {{ gpa }}/4.0</span>
        </div>
    </div>
</template>

<script lang="ts">
import { Vue } from 'vue-class-component';
import { Prop } from 'vue-property-decorator';

export default class EducationEntry extends Vue {
    @Prop() university !: string;
    @Prop() address !: string;
    @Prop() college !: string;
    @Prop() degreeName !: string;
    @Prop() graduationDate !: string;
    @Prop() gpa !: number;
}
</script>