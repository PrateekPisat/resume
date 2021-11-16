<template>
    <tr>
        <td class="font-bold">{{ header }}:</td>
        <td>{{ details.join(", ") }}.</td>
    </tr>
</template>
<script lang="ts">
import { Vue } from 'vue-class-component';
import { Prop } from 'vue-property-decorator';

export default class EducationEntry extends Vue {
    @Prop() header!: string;
    @Prop() details!: string[];
}
</script>