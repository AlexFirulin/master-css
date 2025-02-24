<template>
  <section class="section-stories">
    <div class="bg-video">
                    <video class="bg-video__content" autoplay muted loop>
                    
                        <source src="../video2.mp4" type="video/mp4">
                        Your browser is not supported!
                    </video>
                </div>
    <div class="u-center-text u-margin-bottom-huge">
      <h2 class="heading-secondary">We make people genuinely happy</h2>
    </div>
    <div class="row">
      <div class="story" v-for="item in items" :key="item.name">
        <figure class="story__shape">
            <img :src="item.image" alt="Person on a tour" class="story__img">
            <figcaption class="story__caption"> {{ item.name }}</figcaption>
        </figure>
        <div class="story__text">
          <h3 class="heading-tertiary u-margin-bottom-small">
            {{ item.text }}
          </h3>
          <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit voluptates
            alias.Lorem ipsum dolor sit amet consectetur adipisicing elit
            voluptates alias.
            Lorem ipsum dolor sit amet consectetur adipisicing elit voluptates
            alias.Lorem ipsum dolor sit amet consectetur adipisicing elit
            voluptates alias
          </p>
        </div>
      </div>
    </div>
    <div class="u-center-text u-margin-top-huge">
      <a class="btn-text">Read all stories &rarr;</a>
    </div>
  </section>
</template>

<script setup lang="ts">
import video from '../video.mp4'
import { ref } from 'vue';

const items = ref([
  {
    name: 'Mary Smith',
    image: '/src/assets/images/nat-8.jpg',
    text: 'I had the best week ever with my family',
  },
  {
    name: 'Jack Wilson',
    image: '/src/assets/images/nat-9.jpg',
    text: 'WOW! My life is completely different now',
  },
  {
    name: 'Sara Jones',
    image: 'src/assets/images/nat-10.jpg',
    text: 'I had the best week ever with my family',
  }
]);
</script>


<style lang="scss" scoped>
@use "../assets/styles/abstracts/variables" as *;
.section-stories {
  background-color: $color-grey-light-1;
  padding: 25rem 0;
  position: relative;
}
</style>
