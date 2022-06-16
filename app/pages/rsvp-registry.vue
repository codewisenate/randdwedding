<template>
  <div style="display: flex">
    <div style="width: 62%">
      <iframe
        src="https://www.online-rsvp.com/event/index.php?event_id=3852&embed=1&token=706b7dbb5fd2dcd69c6fb72562656e4e"
        style="min-height: 80vh; width: 100%; border: none"
        title="Online RSVP event form"
        onload="this.style.height=(document.querySelector('.main').offsetHeight -
document.querySelector('header').offsetHeight -
document.querySelector('footer').offsetHeight)+'px';"
      ></iframe>
    </div>
    <div style="margin-top: 8rem; text-align: center; width: 33%; padding-left: 2%;">
      <h1>RSVP & Registry</h1>
      <h2>Interested in the gift registry?</h2>
      <p>
        If you would like to purchase an item off the registry, please indicate that it
        has been purchased on the registry item’s page by selecting “I have bought this
        gift already” for the convenience of other guests.
      </p>
      <button
        class="registry-btn"
        onclick="window.location = 'https://www.myregistry.com/wedding-registry/denielle-hill-and-rowan-king-vancouver-british-columbia/2556670'"
      >
        <i class="icon-present icons"></i>
        Visit the Gift Registry
      </button>
    </div>
  </div>
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

iframe {
  background-color: rgba($white, 0.95);
  border-radius: 6px 6px 0 0;
  margin-right: 1rem;
}

.registry-btn {
  background-color: rgb(141, 160, 110);
  color: white;
  border-radius: 3px;
  padding: 0.75em 30px;
  display: inline-block;
  max-height: 55px;
  transition: all 0.2s;
  margin: 3rem auto 0;
  font-style: italic;

  &::before {
    content: "\e02f";
    font-family: simple-line-icons;
    margin-right: 6px;
    color: lightgray;
    transition: color 0.2s;
    font-style: normal;
    vertical-align: -1px;
  }

  &:hover {
    background-color: hsl(82, 20%, 42%);
    transform: translateY(-3px);
    vertical-align: -1px;
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