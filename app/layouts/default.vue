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

body {
  transition: background 0.3s linear;
  background-color: $darkgreen;
  background-size: contain;
  background-repeat: no-repeat;
  background-position: center 200px;
  @media (min-width: 768px) {
    background-size: cover;
    background-attachment: fixed;
  }
  &.home {
    background-image: url(../static/images/home-bg-1.jpg);
    @media (min-width: 768px) {
      background-position: center;
    }
  }
  &.rsvp {
    background-image: url(../static/images/rsvp-bg-3.jpg);
    @media (min-width: 768px) {
      background-position: center;
    }
  }
  &.venue {
    background-image: url(../static/images/venue-bg-2.jpg);
    @media (min-width: 768px) {
      background-position: 60%;
    }
  }
  &.travel {
    background-image: url(../static/images/travel-bg-2.jpg);
    @media (min-width: 768px) {
      background-position: 60%;
    }
  }
  &.activities {
    background-image: url(../static/images/activities-bg-1.jpg);
    @media (min-width: 768px) {
      background-position: 30%;
    }
  }
  &.covid {
    background-image: url(../static/images/covid-bg-2.jpg);
    @media (min-width: 768px) {
      background-position: 30%;
    }
  }
  .footer {
    background: url(../static/images/home-bg-1.jpg),  url(../static/images/rsvp-bg-3.jpg), url(../static/images/venue-bg-2.jpg), url(../static/images/travel-bg-2.jpg), url(../static/images/activities-bg-1.jpg), url(../static/images/covid-bg-2.jpg);
    background-blend-mode: hue;
  }
}

* {
  font-family: "Cormorant Upright";
}
.markdown h1 {
  font-size: 11vw;
  @media (min-width: 768px) {
    font-size: 4rem;
  }
  line-height: 1;
  padding-bottom: 1rem;
}

.markdown h2 {
  font-size: 9vw;
  @media (min-width: 768px) {
    font-size: 29px;
  }
  padding-bottom: 1rem;
}

 h1, h2, h3, p, li, span, a {
    color: $white;
    text-shadow: 2px 2px 4px $black, 0px 0px 10px rgba($black, 0.33), 0px 0px 30px rgba($black, 0.1);
    &:focus {
      text-shadow: 2px 2px 4px rgba($black, 0.8);
    }
  }

p,
li,
span {
  font-size: 1.66rem;
}

a {
  color: $white;
}

#content {
  background: linear-gradient(20deg, rgba($darkgreen,0.99) 20%, rgba($darkgreen,0.2) 100%);
  border-left: 4px solid $darkgreen;
  border-radius: 6px;
}

body.travel #content {
  background: linear-gradient(20deg, rgba($darkgreen,0.99) 90%, rgba($darkgreen,0.2) 100%);
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
