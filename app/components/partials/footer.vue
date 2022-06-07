<template>
  <footer class="footer -mx-4 md:mx-0">
    <div class="container mx-auto pb-6 flex justify-center">
      &copy; 2022 rowan & denielle — site made with <span class="emoji" role="img">❤️</span> by mum
      and dad
    </div>
  </footer>
</template>

<script lang="ts">
import { Component, Vue } from 'nuxt-property-decorator';

@Component
export default class Footer extends Vue {}
</script>

<style lang="scss">
.footer {
  background-color: $edwardiangreen;
  color: rgba(#fff, 0.66);
  font-size: 1rem;
  font-weight: 100;
  padding-top: 1.75rem;
  .emoji {
    display: inline-block;
    font-size: 0.8rem;
    position: relative;
    top: 4px;
    margin: 0 2px;
  }
}
</style>
