<template>
  <section class="section-tours">
    <div class="u-center-text u-margin-bottom-big">
      <h2 class="heading-secondary">Most popular tours</h2>
    </div>
    <div class="row">
      <div class="col-1-of-3" v-for="(item, index) in items" :key="index">
        <div class="card">
          <div class="card__side card__side--front">
            <div class="card__picture" :class="'card__picture--' + (index + 1)">
              &nbsp;
            </div>
            <h4 class="card__heading">
              <span
                class="card__heading-span"
                :class="'card__heading-span' + (index + 1)"
              >
                {{ item.title }}</span
              >
            </h4>
            <div class="card__details">
              <ul>
                <li v-for="i in item.details">
                  {{ i }}
                </li>
              </ul>
            </div>
          </div>
          <div
            class="card__side card__side--back"
            :class="'card__side--back-' + (index + 1)"
          >
            <div class="card__cta">
              <div class="card__price-box">
                <p class="card__price-only">Only</p>
                <p class="card__price-value">$297</p>
              </div>

              <a href="#" class="btn btn--white">Book now!</a>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="u-center-text u-margin-top-huge">
      <a href="#" class="btn btn--green">Discover all tours</a>
      </div>
  </section>
</template>

<script lang="ts" setup>
import { reactive } from "vue";

const items = reactive([
  {
    icon: "icon-basic-world",
    title: "Explore the world",
    details: [
      "3 day tours",
      "Up to 30 people",
      "2 Tour guides",
      "Sleep in cozy hotels",
      "Difficulty: easy",
    ],
    text: "Lorem ipsum dolor sit amet consectetur adipisicing elit!",
  },
  {
    title: "Meet nature",
    details: [
      "7 day tours",
      "Up to 40 people",
      "6 Tour guides",
      "Sleep in provided tents",
      "Difficulty: medium",
    ],
  },
  {
    title: "Find your way",
    details: [
      "5 day tours",
      "Up to 15 people",
      "3 Tour guides",
      "Sleep in provided tents",
      "Difficulty: hard",
    ],
  },
  //   {
  //     icon: "icon-basic-compass",
  //     title: "Meet nature",
  //     text: "Lorem ipsum dolor sit amet consectetur adipisicing elit!",
  //   },
  //   {
  //     icon: "icon-basic-map",
  //     title: "Find your way",
  //     text: "Lorem ipsum dolor sit amet consectetur adipisicing elit!",
  //   },
]);
</script>

<style lang="scss" scoped>
@use "./../assets/styles/abstracts/variables" as *;

.section-tours {
  background-color: $color-grey-light-1;
  padding: 25rem 0;
  margin-top: -15rem;
}

.card__picture--1 {
  background-image: linear-gradient(
      to right bottom,
      $color-secondary-light,
      $color-secondary-dark
    ),
    url(../assets/images/image5.jpg);
}

.card__picture--2 {
  background-image: linear-gradient(
      to right bottom,
      $color-primary-light,
      $color-primary-dark
    ),
    url(../assets/images/nat-6.jpg);
}

.card__picture--3 {
  background-image: linear-gradient(
      to right bottom,
      $color-tertiary-light,
      $color-tertiary-dark
    ),
    url("../assets/images/nat-7.jpg");
}
</style>
