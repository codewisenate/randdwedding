<template>
  <section class="event-details">
    <div class="py-24 md:py-36 mx-auto flex flex-wrap flex-col items-start">
      <div id="content"
        class="px-6 shadow-md flex flex-col w-full lg:w-3/5 markdown mt-24 md:mt-0"
      >
        <h1>Our Wedding Album</h1>
       <p>Thank you to everyone who joined us to celebrate our big day! It meant a lot to have so many of the people we love with us for our ceremony and afternoon tea. Travel back in time with us once more and peruse these memories from the day at your leisure…</p>

        <p>*More photos to come! Save this page in your bookmarks and visit later as we receive the rest of the collection.</p>

        <div class='image-container'><img src='../assets/images/01.jpg' /></div>
        <div class='image-container'><img src='../assets/images/02.jpg' /></div>
        <div class='image-container'><img src='../assets/images/03.jpg' /></div>
        <div class='image-container'><img src='../assets/images/04.jpg' /></div>
        <div class='image-container'><img src='../assets/images/05.jpg' /></div>
        <div class='image-container'><img src='../assets/images/06.jpg' /></div>
        <div class='image-container'><img src='../assets/images/07.jpg' /></div>
        <div class='image-container'><img src='../assets/images/08.jpg' /></div>
        <div class='image-container'><img src='../assets/images/09.jpg' /></div>
        <div class='image-container'><img src='../assets/images/10.jpg' /></div>
        <div class='image-container'><img src='../assets/images/11.jpg' /></div>
        <div class='image-container'><img src='../assets/images/12.jpg' /></div>
        <div class='image-container'><img src='../assets/images/13.jpg' /></div>
        <div class='image-container'><img src='../assets/images/14.jpg' /></div>
        <div class='image-container'><img src='../assets/images/15.jpg' /></div>
        <div class='image-container'><img src='../assets/images/16.jpg' /></div>
        <div class='image-container'><img src='../assets/images/17.jpg' /></div>
        <div class='image-container'><img src='../assets/images/18a.jpg' /></div>
        <div class='image-container'><img src='../assets/images/18b.jpg' /></div>
        <div class='image-container'><img src='../assets/images/19.jpg' /></div>
        <div class='image-container'><img src='../assets/images/20a.jpg' /></div>
        <div class='image-container'><img src='../assets/images/20b.jpg' /></div>
        <div class='image-container'><img src='../assets/images/20c.jpg' /></div>
        <div class='image-container'><img src='../assets/images/20d.jpg' /></div>
        <div class='image-container'><img src='../assets/images/21.jpg' /></div>
        <div class='image-container'><img src='../assets/images/22.jpg' /></div>
        <div class='image-container'><img src='../assets/images/23.jpg' /></div>
        <div class='image-container'><img src='../assets/images/24.jpg' /></div>
        <div class='image-container'><img src='../assets/images/25.jpg' /></div>
        <div class='image-container'><img src='../assets/images/26.jpg' /></div>
        <div class='image-container'><img src='../assets/images/27.jpg' /></div>
        <div class='image-container'><img src='../assets/images/28.jpg' /></div>
        <div class='image-container'><img src='../assets/images/29a.jpg' /></div>
        <div class='image-container'><img src='../assets/images/29b.jpg' /></div>
        <div class='image-container'><img src='../assets/images/29c.jpg' /></div>
        <div class='image-container'><img src='../assets/images/29d.jpg' /></div>
        <div class='image-container'><img src='../assets/images/30.jpg' /></div>
        <div class='image-container'><img src='../assets/images/31.jpg' /></div>
        <div class='image-container'><img src='../assets/images/32.jpg' /></div>

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
        class: 'travel'
      }
    }
  };
}
</script>

<style scoped>
  .resimKutusu {
    border: 1px solid #cdcdcd;
    padding: 5px;
    background: #eeeeee;
    border-radius: 5px;
    cursor: pointer;
  }
  </style>