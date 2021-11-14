<template>
  <div>
    <p class="text-3xl font-bold text-center">{{ name }}</p>
    <p class="text-center">
      <span><i class="fas fa-map-marked"></i> {{ address }} </span> | 
      <span><i class="fas fa-phone-square-alt fa-lg"></i> {{  phoneNumber }} </span> | 
      <span><i class="fas fa-envelope-square fa-lg"></i> {{ emailId }} </span> | 
      <span><a :href="linkedInURL" target="_blank"><i class="fab fa-linkedin fa-lg"></i></a></span> | 
      <span><a :href="githubURL"><i class="fab fa-github-square fa-lg"></i></a></span>
    </p>
  </div>
</template>

<script lang="ts">
import { Vue } from 'vue-class-component';
import { Prop } from 'vue-property-decorator';

export default class Header extends Vue {
  @Prop() name!: string
  @Prop() address!: string
  @Prop() emailId!: string
  @Prop() phoneNumber!: string
  @Prop() linkedInURL!: string
  @Prop() githubURL!: string
}
</script>