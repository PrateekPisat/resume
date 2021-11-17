<template>
    <div>
        <EntryHeader :university="title" :address="address" :college="companyName" :graduationDate="duration"/>
        <div class="space-x-6" v-for="detail in details" :key=detail>
            <i class="fas fa-circle fa-sm"></i> 
            <span>{{ detail }}</span>
        </div>
        <br>
    </div>
</template>
<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import { Prop } from 'vue-property-decorator';
import EntryHeader from './EntryHeader.vue'

@Options({components: {EntryHeader}})
export default class EducationEntry extends Vue {
    @Prop() title!: string;
    @Prop() companyName !: string;
    @Prop() address !: string;
    @Prop() duration !: string;
    @Prop() details!: string[];
}
</script>