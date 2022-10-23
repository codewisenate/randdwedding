<template>
  <section class="event-details">
    <div class="py-24 md:py-36 mx-auto flex flex-wrap flex-col items-start">
      <div id="content"
        class="px-6 shadow-md flex flex-col w-full lg:w-3/5 markdown mt-24 md:mt-0"
      >
        <h1>Our Wedding Album</h1>
       <p>Thank you to everyone who joined us to celebrate our big day! It meant a lot to have so many of the people we love with us for our ceremony and afternoon tea. Travel back in time with us once more and peruse these memories from the day at your leisure…</p>

       <p class='largescreen'>Click to enlarge images and press tab (or use arrow keys) to progress through them.</p>

        <p>*More photos to come! Save this page in your bookmarks and visit later as we receive the rest of the collection.</p>
        <div class='gallery' @keydown='checkKey'>
        <div class='image-container' tabindex="0"><img src='../assets/images/01.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/02.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/03.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/33.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/04.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/06.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/07.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/08.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/38.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/39.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/05.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/09.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/10.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/37.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/34.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/35.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/36.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/40.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/41.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/42.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/43.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/11.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/12.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/44.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/45.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/46.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/47.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/48.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/49.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/50.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/51.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/52.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/53.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/13.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/14.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/15.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/58.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/59.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/16.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/17.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/60.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/63.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/62.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/64.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/61.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/65.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/66.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/54.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/55.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/56.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/57.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/67.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/68.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/69.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/18a.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/18b.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/19.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/20a.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/20b.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/20c.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/20d.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/21.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/22.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/23.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/24.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/25.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/70.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/71.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/26.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/27.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/28.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/72.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/136.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/137.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/29b.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/29c.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/29a.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/29d.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/73.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/74.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/75.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/76.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/77.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/78.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/79.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/80.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/81.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/82.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/83.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/84.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/85.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/86.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/87.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/88.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/89.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/90.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/91.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/92.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/93.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/94.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/95.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/96.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/97.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/98.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/99.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/100.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/101.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/102.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/103.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/104.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/105.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/106.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/107.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/108.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/109.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/110.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/111.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/112.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/113.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/114.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/115.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/116.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/117.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/118.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/119.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/120.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/121.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/122.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/123.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/124.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/125.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/126.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/127.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/128.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/129.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/130.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/131.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/132.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/133.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/134.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/135.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/30.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/31.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/32.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/138.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/139.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/140.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/141.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/143.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/144.jpg' /></div>
        <div class='image-container' tabindex="0"><img src='../assets/images/145.jpg' /></div>
      </div>
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
  }
  checkKey(e) {

    e = e || window.event;
    const currentEl = document.activeElement;
    const prevEl = currentEl?.previousElementSibling;
    const nextEl = currentEl?.nextElementSibling;
    if (e.keyCode == '38' || e.keyCode == '37') {
        // up / left arrow
        if (null !== prevEl) { 
          prevEl?.focus(); 
        } else { 
          if (null !== currentEl) { currentEl?.blur(); }
        }
    }
    if (e.keyCode == '40' || e.keyCode == '39') {
        // down / right arrow
        if (null !== nextEl) { 
          nextEl?.focus(); 
        } else { 
          if (null !== currentEl) { currentEl?.blur(); }
        }
    }
    if (e.keyCode == '27') {
        // esc
        if (null !== currentEl) { currentEl?.blur(); }
    }
  }
}

 

</script>

<style lang='scss' scoped>
.gallery {
  display: grid;
  gap: 1rem;
  grid-template-columns: 1fr;
  @media (min-width: 640px) {
    grid-template-columns: 1fr 1fr 1fr;
  }
}
.largescreen {
  display: none;
  @media (min-width: 640px) {
    display: block;
  }
}
.image-container {
  @media (min-width: 640px) {
    height: auto;
    display: flex;
  }
}
img {
  @media (min-width: 640px) {
    max-width: 100%;
    height: auto;
    object-fit: cover;
    transform: all 0.3s ease;
  }
}
.image-container:focus img {
  @media (min-width: 640px) {
    position: fixed;
    margin: auto;
    left: 0;
    right: 0;
    height: 90vh;
    box-shadow: 0 0 8px #333;
    top: calc(5% + -1rem);
    max-width: 90%;
  }
}
.image-container:focus::after  {
  @media (min-width: 640px) {
    content: "X";
    font-family: sans-serif;
    font-size: 1.5rem;
    font-weight: 900;
    text-shadow: 0 0 8px #333;
    display: block;
    position: fixed;
    color: white;
    top: 2rem;
    right: 2rem;
    z-index: 999;
    pointer-events: none;
    cursor: pointer;
  }
}
  </style>