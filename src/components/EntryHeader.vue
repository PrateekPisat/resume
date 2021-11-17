<template>
    <div class="inline-block float-left">
            <span class="font-bold">{{ university }}, </span>
            <span>{{ address }}</span>
    </div>
    <div class="inline-block float-right">{{ graduationDate }}</div>
    <br>
    <div>{{ college }}</div>
</template>

<script lang="ts">
import { Vue } from 'vue-class-component';
import { Prop } from 'vue-property-decorator';

export default class EducationEntry extends Vue {
    @Prop() university !: string;
    @Prop() address !: string;
    @Prop() college !: string;
    @Prop() graduationDate !: string;
}
</script>