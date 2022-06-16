<template>
  <section class="home">
    <div class="py-24 md:py-36 mx-auto flex flex-wrap flex-col justify-end items-end">
      <div class="w-full xl:w-5/12 flex flex-col">
        <h1>Rowan &amp; Denielle's Wedding</h1>
        <h2>Tying the knot, <br />11th of September, 2022 <br />...in Edwardian fashion amidst the trees and by the sea.</h2>
      </div>
    </div>
  </section>
</template>


<style lang="scss" scoped>
h1 {
  font-size: 6rem;
}
h2 {
  font-size: 2.75rem;
  line-height: 1.5;
}
</style>

<script lang="ts">
import { Component, Vue } from 'nuxt-property-decorator';

@Component({
  // Called to know which transition to apply
  transition() {
    return 'slide-left';
  },
})

export default class Home extends Vue {
  
  head () {
    return {
      bodyAttrs: {
        class: 'home'
      }
    }
  };
}
</script>
