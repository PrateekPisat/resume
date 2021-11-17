<template>
    <div>
        <EntryHeader :university="university" :address="address" :college="college" :graduationDate="graduationDate"/>
        <div>
            <span class="italic">{{ degreeName }}</span>
            <span>, GPA: {{ gpa }}/4.0</span>
        </div>
    </div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import { Prop } from 'vue-property-decorator';
import EntryHeader from './EntryHeader.vue'

@Options({components: {EntryHeader}})
export default class EducationEntry extends Vue {
    @Prop() university !: string;
    @Prop() address !: string;
    @Prop() college !: string;
    @Prop() degreeName !: string;
    @Prop() graduationDate !: string;
    @Prop() gpa !: number;
}
</script>