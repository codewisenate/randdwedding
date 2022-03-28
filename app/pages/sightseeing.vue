<template>
  <section class="event-details">
    <div class="py-24 md:py-36 mx-auto flex flex-wrap flex-col md:flex-row items-center">
      <div
        class="flex flex-col w-full xl:w-3/5 justify-center lg:items-start overflow-y-hidden markdown"
      >
        <h1>Things to see</h1>
      </div>
      <div class="flex flex-col w-full xl:w-2/5">
        <img alt="Hero" class="rounded shadow-xl" src="/images/uploads/selfie.jpg" />
      </div>
    </div>
  </section>
</template>

<script lang="ts">
import { Component, Vue } from 'nuxt-property-decorator';

@Component({
  // Called to know which transition to apply
  transition() {
    return 'slide-left';
  },
})
export default class Home extends Vue {}
</script>
