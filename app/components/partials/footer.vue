<template>
  <footer class="footer -mx-4 md:mx-0">
    <div class="container mx-auto px-6 pb-6 flex flex-col md:flex-row justify-center items-center">
      <div class="text-center">&copy; 2022 rowan & denielle — site made with <span class="emoji" role="img">🤍</span> by mum
      and dad</div>
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
  background-color: $darkgreen !important;
  color: rgba(#fff, 1);
  font-size: 1.25rem;
  font-weight: 100;
  padding-top: 1.75rem;
  span {
    text-shadow: none;
  }
  .emoji {
    display: inline-block;
    color: #fff;
    font-size: 0.8rem;
    position: relative;
    top: 0;
    margin: 0 2px;
  }
}
</style>
