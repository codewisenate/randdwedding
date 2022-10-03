<template>
  <header class="flex items-start md:items-center py-4 md:py-8 sm:items-start">
    <div class="header__logo">
      <nuxt-link to="/">
        <img :src="logo" class="logo mt-4 md:mt-0" alt="Rowan and Denielle's wedding website" />
      </nuxt-link>
    </div>

    <nav class="nav ml-auto">
      <ul class="flex flex-col md:flex-row items-center sm:mt-4 sm:pt-4 md:mt-0 md:pt-0 md:mr-4 lg:mr-8 text-center">
        <!-- <li>
          <nuxt-link to="/rsvp-registry" class="block font-medium px-4 py-1 md:p-2 lg:px-4">
            RSVP & Registry
          </nuxt-link>
        </li> -->
        <li>
          <nuxt-link to="/album" class="block font-medium px-4 py-1 md:p-2 lg:px-4">
            Wedding Album
          </nuxt-link>
        </li>
        <li>
          <nuxt-link to="/event-details" class="block font-medium  px-4 py-1 md:p-2 lg:px-4">
            Cecil Green Park House
          </nuxt-link>
        </li>
        <li>
          <nuxt-link to="/activities" class="block font-medium  px-4 py-1 md:p-2 lg:px-4">
            Venue Nearby Activities
          </nuxt-link>
        </li>
        <!-- <li>
          <nuxt-link to="/covid" class="block font-medium  px-4 py-1 md:p-2 lg:px-4">
            COVID
          </nuxt-link>
        </li> -->
        <!-- <li
          v-for='(page, index) in pages'
          :key='index'
          class='block font-medium px-4 py-1 md:p-2 lg:px-4'
        >
          <nuxt-link :to='`/${page.slug}`'>{{ page.title }}</nuxt-link>
        </li> -->
      </ul>
    </nav>
  </header>
</template>

<script lang="ts">
import { Component, Vue } from 'nuxt-property-decorator';
import settings from '@/content/settings/general.json';

@Component
export default class Header extends Vue {
  get pages(): Page[] {
    return this.$store.state.pages;
  }

  logo = settings.logo;
}
</script>

<style lang="scss" scoped>
.logo {
  height: 42px;
}
.nav {
  ul li > a {
    color: $white;
    line-height: 1.25;
    white-space: nowrap;
    @media (min-width: 768px) {
      white-space: normal;
    }
    @media (max-width: 768px) {
      font-size: 1.33rem;
    }
    &.nuxt-link-active {
      color: $white;
      @apply font-bold;
      text-decoration: underline;
    }
  }
}
</style>
