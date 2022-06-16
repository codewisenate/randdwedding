<template>
  <section class="event-details">
    <div class="py-24 md:py-36 mx-auto flex flex-wrap flex-col items-end">
      <div id="content"
        class="px-6 shadow-md flex flex-col w-full xl:w-2/5 markdown"
      >
        <h1>COVID</h1>
        <p>
          We are excited to see you on the big day! We would like to acknowledge there is
          still risk of transmission and we hope to make our wedding a safe and enjoyable
          event for everyone.
        </p>
        <ul>
          <li>
            We ask that guests bring and wear face masks for indoor use except while
            eating and drinking.
          </li>
          <li>
            Ceremony and cocktail hour will take place outside, and afternoon tea will
            take place indoors; you are welcome to choose to attend the outdoor portions
            of the event if this is more comfortable. Please simply specify which event
            activities you are joining on the RSVP form.
          </li>
          <li>Hand sanitizer will be provided in key locations.</li>
        </ul>
      </div>
      <div class="flex flex-col w-full xl:w-2/5"></div>
    </div>
  </section>
</template>

<style lang="scss" scoped></style>

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
        class: 'covid'
      }
    }
  };
}
</script>
