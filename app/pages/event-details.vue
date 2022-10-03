<template>
  <section class="event-details">
    <div class="py-24 md:py-36 mx-auto flex flex-wrap flex-col md:flex-row items-center">
      <div id="content"
        class="px-6 shadow-md flex flex-col w-full lg:w-2/5 justify-center lg:items-start markdown mt-24 md:mt-0"
      >
        <h1>Venue History</h1>

        <h2>
          <a href="https://cecilgreenpark.ubc.ca/">Cecil Green Park House</a><br />“The House
          on the Cliff”
        </h2>
        <p>
          View:
          <a
            href="https://www.google.com/maps/place/Cecil+Green+Park+House/@49.2713887,-123.2598931,17z/data=!3m1!4b1!4m5!3m4!1s0x548672b1a4606653:0xba00269da2e1e9f0!8m2!3d49.2713233!4d-123.257706"
            >Google map</a
          >.
        </p>

        <h2>Venue Early History</h2>
        <p>
          Edward Pease Davis, a prominent barrister, solicitor and courtroom lawyer and
          founder of the law firm EP Davis and Company, purchased, along with a Dr.
          Lefevre, ten acres of crown land on the tip of Point Grey Cliffs in order to
          escape from the increasingly crowded west end of Vancouver and the
          then-fashionable migration to Shaughnessy Heights. The house was commissioned in
          1912 and was designed by Samuel Maclure, one of British Columbia’s most prolific
          architects in the early part of the 20th century. Davis named the house Kanakla,
          a Coast Salish word meaning “house on the cliff.”
        </p>
        <p>
          In 1912, the public tram line ended at 4th at Alma from where guests to Kanakla
          either had to walk or were collected by the Davis’ car. Electricity was not
          installed until the 1920s and until that time, gas for lighting was manufactured
          in a small building purpose-built between the east of the house and the squash
          court building. (The gas house, along with the game larders on the north side of
          the structure were restored in 2003.) Residents drew their water from a stream
          that flowed across what is now the UBC campus, and used wood and coal for
          heating and cooking.
        </p>
        <p>
          A staff of three ran Kanakla; the cook, the butler / chauffer and the gardener.
          The gardener and his family lived over the garage, located at the west end of
          the driveway. He was responsible for maintaining the extensive grounds that
          included a rose garden and croquet lawn at the northwest corner of the house, as
          well as a formal Italian garden, with tennis and badminton courts to the north
          east.
        </p>
        <p>
          Since 1912, cliff erosion has taken about two thirds of the original garden
          area, as well as the end of the west driveway.
        </p>
      </div>
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
        class: 'venue'
      }
    }
  };
}
</script>