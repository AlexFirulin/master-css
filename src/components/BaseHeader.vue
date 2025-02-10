<script setup lang="ts">
import BaseHeaderButton from './Buttons/BaseHeaderButton.vue';

</script>

<template>
  <header class="header">
    <div class="header__logo-box">
      <img src="../assets/images/logo-white.png" alt="logo" class="header__logo" />
    </div>
    <div class="header__text-box">
      <h1 class="heading-primary">
        <span class="heading-primary--main">Outdoors</span>
        <span class="heading-primary--sub">is where life happens</span>
      </h1>
      <BaseHeaderButton />
    </div>
  </header>
</template>

<style scoped lang="scss">

</style>
