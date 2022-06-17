<template>
  <section class="event-details">
    <div class="py-24 md:py-36 mx-auto flex flex-wrap flex-col justify-end items-end">
      <div id="content"
        class="shadow-md px-6 flex flex-col items-start justify-items-end justify-end w-full lg:w-2/5  markdown mt-6 md:mt-0"
      >
        <h1>Nearby Activities</h1>
        <h2><a href="http://www.moa.ubc.ca">Museum of Anthropology</a></h2>
        <p>6393 NW Marine Dr, Vancouver</p>
        <p>
          See
          <a
            href="https://www.google.com/maps/place/Museum+of+Anthropology+at+UBC/@49.2695015,-123.2616296,17z/data=!3m2!4b1!5s0x548672b3d24258f9:0x75c952bb4cfbcd8c!4m5!3m4!1s0x548672b3db30ffad:0xf6711cf4e0ad84e3!8m2!3d49.2695015!4d-123.2594409"
            >Google map</a
          >.
        </p>
        <h2><a href="https://botanicalgarden.ubc.ca">UBC Botanical Garden</a></h2>
        <p>6804 SW Marine Drive, Vancouver</p>
        <p>
          See
          <a
            href="https://www.google.com/maps/place/UBC+Botanical+Garden/@49.2543,-123.2527644,17z/data=!3m1!4b1!4m5!3m4!1s0x54860d32ea37f2cd:0xe3151fbda8c2f14f!8m2!3d49.2543!4d-123.2505757"
            >Google map</a
          >.
        </p>
        <h2><a href="http://theboulevard.ca">The Boulevard Coffee Roasters Co.</a></h2>
        <p>5970 University Blvd, Vancouver</p>
        <p>
          See
          <a
            href="https://www.google.com/maps/place/The+Boulevard+Coffee+Roasting+Co/@49.2660099,-123.2485888,17z/data=!3m2!4b1!5s0x548672b7e6d83c45:0xe0823cc15bfd7fc8!4m5!3m4!1s0x548672b640975c65:0x907aba283e1b2e3d!8m2!3d49.2660099!4d-123.2464001"
            >Google map</a
          >.
        </p>
        <h2><a href="https://jjbeancoffee.com/pages/locations#ubc">JJ Bean</a></h2>
        <p>6005 University Blvd, Vancouver</p>
        <p>
          See
          <a
            href="https://www.google.com/maps/place/JJ+Bean+Coffee+Roasters/@49.2663273,-123.2513956,17z/data=!3m1!4b1!4m5!3m4!1s0x548672bbf69924d1:0xf0b2db8921115ce5!8m2!3d49.2663023!4d-123.2469028"
            >Google map</a
          >.
        </p>
        <h2>
          <a
            href="https://www.google.com/maps/place/Wreck+Beach/@49.2621949,-123.2658957,16z/data=!3m1!4b1!4m5!3m4!1s0x54860d4a8f993a53:0xedbf79877941394b!8m2!3d49.2621955!4d-123.2615183"
            >Wreck Beach</a
          >,
          <a
            href="https://www.google.com/maps/place/Tower+Beach,+Vancouver,+BC+V6T+1X8/@49.2725123,-123.2603895,18z/data=!3m1!4b1!4m5!3m4!1s0x548672b1d88a23fb:0xe1e87bd6896f7dab!8m2!3d49.2732579!4d-123.2577551"
            >Tower Beach</a
          >, &
          <a
            href="https://www.google.com/maps/place/Pacific+Spirit+Regional+Park/@49.2532859,-123.2200876,17z/data=!3m1!4b1!4m5!3m4!1s0x54867325cd77a111:0x3398f07bb10b71a0!8m2!3d49.253286!4d-123.2156029"
            >Pacific Spirit Regional Park and trails</a
          >
        </h2>
        <p>
          The beaches and Foreshore trail (via Trail 3) can be accessed from the Cecil Green
          Park House parking lot.
        </p>
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
        class: 'activities'
      }
    }
  };
}
</script>