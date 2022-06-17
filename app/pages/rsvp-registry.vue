<template>
  <section class="rsvp">
    <div class="py-24 md:py-36 mx-auto flex flex-wrap flex-col items-start">
      <div id="content"
        class="px-6 shadow-md flex flex-col w-full lg:w-2/5 markdown mt-6 md:mt-0"
      >
      <h1>RSVP & Registry</h1>
      <p>We hope you’ll join us for our ceremony and afternoon tea! Please click here to RSVP by the 11th of July.</p>
      <button
        class="btn rsvp-btn"
        onclick="window.open('https://rowdenwedding.online-rsvp.com', '_blank').focus();"
      >
        Fill out your RSVP 
      </button>
      <h2 class="mt-1">Interested in the gift registry?</h2>
      <p>
        If you would like to purchase an item off the registry, please indicate that it
        has been purchased on the registry item’s page by selecting “I have bought this
        gift already” for the convenience of other guests.
      </p>
      <button
        class="btn registry-btn"
        onclick="window.open('https://www.myregistry.com/wedding-registry/denielle-hill-and-rowan-king-vancouver-british-columbia/2556670', '_blank').focus();"
      >
        Visit the Gift Registry
      </button>
       <p class="text-center"><small>Buttons open a new tab or window.</small></p>
    </div>
    </div>
  </section>
</template>

<style lang="scss">
hr {
  border: none;
  width: 60%;
  max-width: 400px;
  height: 50px;
  overflow: hidden;
  margin: 0 auto;
  &::after {
    content: "";
    display: block;
    margin: -30px auto 0;
    width: 100%;
    height: 25px;
    border-radius: 150px / 10px;
    box-shadow: 0 0 20px #ccc;
  }
}

.btn {
  background-color: rgba($white, 1);
    border: 1px solid $darkgreen;
  color: $darkgreen;
  border-radius: 3px;
  padding: 0.75em 30px;
  display: inline-block;
  max-height: 55px;
  transition: all 0.2s;
  margin: 2rem auto 2rem;
  font-style: italic;

  &::before {
    font-family: simple-line-icons;
    margin-right: 6px;
    color: $darkgreen;
    transition: color 0.2s;
    font-style: normal;
    vertical-align: -1px;
  }

  &.registry-btn {
    margin: 2rem auto 4rem;
    &::before {
      content: "\e02f";
    }
  }

  &.rsvp-btn::before {
    content: "\e080";
  }

  &:hover {
    background-color: hsl(82, 20%, 42%);
    border: 1px solid $white;
    color: $white;
    transform: translateY(-3px);
    vertical-align: -1px;
    &::before {
      color: $white;
    }
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
        class: 'rsvp'
      }
    }
  };
}
</script>