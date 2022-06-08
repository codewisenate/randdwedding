<template>
  <section class="event-details">
    <div class="py-24 md:py-36 mx-auto flex flex-wrap flex-col md:flex-row items-center">
      <div
        class="flex flex-col w-full xl:w-3/5 justify-center lg:items-start overflow-y-hidden markdown"
      >
        <h1>Accommodation & Travel</h1>
        <h2>Where to stay</h2>
        <h3>
          <a href="http://west-coast-suites-at-ubc.vancouver-hotels-bc.com/en"
            >West Coast Suites</a
          ></h3>
          <p>5959 Student Union Boulevard,<br />Vancouver, Canada</p>
        
        <p>
          View:
          <a
            href="https://www.google.com/maps/place/West+Coast+Suites+at+UBC/@49.2693793,-123.2508493,17z/data=!3m1!4b1!4m8!3m7!1s0x548672b7587c4a57:0x9207ff80cb128484!5m2!4m1!1i2!8m2!3d49.2693713!4d-123.2486542"
            >Google map</a
          >.
        </p>

        <h2>Travel Info</h2>
        <p>
          It’s easiest to reach <nuxt-link to="event-details">Cecil Green</nuxt-link> by
          car.
        </p>
        <h3>Nearby bus routes</h3>
        <p>
          <a
            href="https://www.google.com/maps/dir/UBC+Bus+Loop,+University+Endowment+Lands,+BC//@49.266738,-123.2491364,17.11z/data=!4m9!4m8!1m5!1m1!1s0x548672b787aa42fd:0x38e3cff4a7d52c2d!2m2!1d-123.2474431!2d49.2675373!1m0!3e3"
            >UBC Bus Loop (”UBC Exchange”)</a
          >
          <br />20 minute walk to venue
        </p>
        <ul>
          <li>Route 25</li>
          <li>Route 99</li>
          <li>Route 004</li>
        </ul>
        <p>
          <a
            href="https://www.google.com/maps/search/+WB+NW+Marine+Dr+@+Cecil+Green+Park+Rd+Stop+ID:+51919+/@49.2709528,-123.2576676,18z/data=!3m1!4b1"
            >Cecil Green Park Rd</a
          >
          <br />5 minute walk to venue
        </p>
        <ul>
          <li>Route 68 – Stop# 51919</li>
        </ul>
      </div>
      <div class="flex flex-col w-full xl:w-2/5"></div>
    </div>
  </section>
</template>

<script lang="ts">
import { Component, Vue } from "nuxt-property-decorator";

@Component({
  // Called to know which transition to apply
  transition() {
    return "slide-left";
  },
})
export default class Home extends Vue {}
</script>
