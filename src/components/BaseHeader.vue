<script setup lang="ts">
import BaseHeaderButton from './Buttons/BaseHeaderButton.vue';

</script>

<template>
  <header class="header">
    <div class="logo-box">
      <img src="../assets/images/logo-white.png" alt="logo" class="logo" />
    </div>
    <div class="text-box">
      <h1 class="heading-primary">
        <span class="heading-primary-main">Outdoors</span>
        <span class="heading-primary-sub">is where life happens</span>
      </h1>
      <BaseHeaderButton />
    </div>
  </header>
</template>

<style scoped>
.header {
  position: relative;
  height: 95vh;
  background-image: linear-gradient(to right bottom, #7ed56fc7, #28b485c4),
    url(../assets/images/hero.jpg);
  background-size: cover;
  background-position: top;
  clip-path: polygon(0 0, 100% 0, 100% 75vh, 0 100%);
}

.logo-box {
  position: absolute;
  top: 40px;
  left: 40px;
}

.logo {
  height: 35px;
}

.text-box {
    position: absolute;
    top: 40%;
    left: 50%;
    transform: translate(-50%, -50%);
    text-align: center;
}

.heading-primary {
  color: #fff;
  text-transform: uppercase;
  backface-visibility: hidden;
  margin-bottom: 60px;
}

.heading-primary-main {
  display: block;
  font-size: 60px;
  font-weight: 400;
  letter-spacing: 35px;
  animation-name: moveToLeft;
  animation-duration: 1s;
  animation-timing-function: ease-out;
  /* animation-delay: 1s;
  animation-iteration-count: 3; */
}

.heading-primary-sub {
  display: block;
  font-size: 20px;
  font-weight: 400;
  letter-spacing: 17px;
  animation-name: moveToRight;
  animation-duration: 1s;
  animation-timing-function: ease-out;
}

@keyframes moveToLeft {
    0% {
        opacity: 0;
        transform: translateX(-100px);
    }
    80% {
        transform: translateX(10px);
    }
    100% {
        opacity: 1;
        transform: translate(0);
    }
}

@keyframes moveToRight {
    0% {
        opacity: 0;
        transform: translateX(100px);
    }
    80% {
        transform: translateX(-10px);
    }
    100% {
        opacity: 1;
        transform: translate(0);
    }
}
</style>
