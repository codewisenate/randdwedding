<template>
  <section class="home">
    <div class="py-24 md:py-36 mx-auto flex flex-wrap flex-col md:flex-row items-center">
      <div class="flex flex-col w-full xl:w-3/5 justify-center lg:items-start overflow-y-hidden">
        <h1>Rowan &amp; Denielle's Wedding</h1>
        <h2>Tying the knot, 11th of September, 2022 <br />...in Edwardian fashion amidst the trees and by the sea.</h2>
      </div>
      <div class="flex flex-col w-full xl:w-2/5"></div>
        <!-- <img alt="Hero" class="rounded shadow-xl" src="/images/uploads/selfie.jpg" /> -->
      </div>
    </div>
  </section>
</template>

<script lang="ts">
import { Component, Vue } from 'nuxt-property-decorator';
import settings from '@/content/settings/general.json';

@Component({
  // Called to know which transition to apply
  transition() {
    return 'slide-left';
  },
})
export default class Home extends Vue {
  welcomeText = settings.welcomeText;

  get posts(): Post[] {
    return this.$store.state.posts;
  }

  encode(data): string {
    return Object.keys(data)
      .map((key) => `${encodeURIComponent(key)}=${encodeURIComponent(data[key])}`)
      .join('&');
  }
}
</script>
