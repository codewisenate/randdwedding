<template>
  <section class="home">
    <div class="py-24 md:py-36 mx-auto flex flex-wrap flex-col justify-end items-end">
      <div id="content" 
      class="p-6 shadow-md w-full lg:w-5/12 flex flex-col mt-24 md:mt-0">
        <h1>Rowan &amp; Denielle's Wedding</h1>
        <h2>Tying the knot, <br />11th of September, 2022 <br />...in Edwardian fashion amidst the trees and by the sea.</h2>
      </div>
    </div>
  </section>
</template>


<style lang="scss" scoped>
h1 {
  font-size: 18vw !important;
  line-height: 1.1;
  margin-bottom: 1rem;
  @media (min-width: 768px) {
    font-size: 6rem !important;
  }
}
h2 {
  font-size: 8vw !important;
  line-height: 1.25;
  @media (min-width: 768px) {
    font-size: 2.5rem !important;
  }
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
