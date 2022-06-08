<template>
  <main :class="[$route.name]" class="main px-4 md:px-0 flex flex-col">
    <site-header class="container mx-auto" />
    <div class="container mx-auto flex-1">
      <nuxt class="nuxt" />
    </div>
    <site-footer />
  </main>
</template>

<script lang="ts">
import { Component, Vue } from "nuxt-property-decorator";
import SiteHeader from "@/components/partials/header.vue";
import SiteFooter from "@/components/partials/footer.vue";

@Component({
  components: {
    SiteHeader,
    SiteFooter,
  },
})
export default class DefaultLayout extends Vue {}
</script>

<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Cormorant+Upright");

@font-face {
  font-family: "simple-line-icons";
  src: url("https://cdnjs.cloudflare.com/ajax/libs/simple-line-icons/2.0.0/fonts/Simple-Line-Icons.eot?-i3a2kk");
  src: url("https://cdnjs.cloudflare.com/ajax/libs/simple-line-icons/2.0.0/fonts/Simple-Line-Icons.eot?#iefix-i3a2kk")
      format("embedded-opentype"),
    url("https://cdnjs.cloudflare.com/ajax/libs/simple-line-icons/2.0.0/fonts/Simple-Line-Icons.ttf?-i3a2kk")
      format("truetype"),
    url("https://cdnjs.cloudflare.com/ajax/libs/simple-line-icons/2.0.0/fonts/Simple-Line-Icons.woff?-i3a2kk")
      format("woff"),
    url("https://cdnjs.cloudflare.com/ajax/libs/simple-line-icons/2.0.0/fonts/Simple-Line-Icons.svg?-i3a2kk#simple-line-icons")
      format("svg");
  font-weight: normal;
  font-style: normal;
}

[class^="icon-"],
[class*=" icon-"] {
  font-family: "simple-line-icons";
  speak: none;
  font-style: normal;
  font-weight: normal;
  font-variant: normal;
  text-transform: none;
  line-height: 1;

  /* Better Font Rendering =========== */
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

* {
  font-family: "Cormorant Upright";
}
h1 {
  font-size: 48px;
  padding-bottom: 1rem;
}

h2 {
  font-size: 29px;
  padding-bottom: 1rem;
}

p,
li,
span {
  color: rgb(82, 82, 82);
  font-size: 1.3rem;
}
a {
  color: $linkgreen;
}

.divider {
  position: relative;
  min-width: 100vw;
  margin-top: auto;
}

.nuxt {
  transition: all 0.5s cubic-bezier(0.55, 0, 0.1, 1);
}
</style>
