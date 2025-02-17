<template>
  <section class="features_section">
    <div class="row">
      <div v-for="(item) in items " class="col-1-of-4">
        <div class="features-box">
          <i class="features-box__icon" :class="item.icon"></i>
          <h3 class="heading-tertiary u-margin-bottom-small">{{ item.title }}</h3>
          <p class="feature-box__text">
           {{ item.text }}
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const items = ref([{
    icon: 'icon-basic-world',
    title: 'Explore the world',
    text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit!'
    }, {
    icon: 'icon-basic-compass',
    title: 'Meet nature',
    text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit!'
    }, {
    icon: 'icon-basic-map',
    title: 'Find your way',
    text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit!'
    }, {
    icon: 'icon-basic-heart',
    title: 'Live a healthier life',
    text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit!'
}]);
</script>

<style lang="scss" scoped>
@use '../assets/styles/abstracts/variables' as *;

.features_section {
    background-color: $color-grey-light-1;
        padding: 20rem 0;
        margin-top: -20vh;
        background-image: linear-gradient(to right bottom, #7ed56fc7, #28b485c4),
        url('../assets/images/nat-4.jpg');
        background-size: cover;
        transform: skewY(-7deg);
        & > * {
            transform: skewY(7deg);
        }
}
</style>
