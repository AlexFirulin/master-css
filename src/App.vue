<script setup lang="ts">
import BaseInfo from './components/BaseInfo.vue';
import BookingSection from './components/BookingSection.vue';
import FeatureSection from './components/FeatureSection.vue';
import StoriesSection from './components/StoriesSection.vue';
import ToursInfo from './components/ToursInfo.vue';
import Default from './layouts/default.vue';


</script>

<template>
    <Default>
        <main>
            <BaseInfo />
            <FeatureSection />
            <ToursInfo />
            <StoriesSection />
            <BookingSection />
        </main>
    </Default>
</template>

<style scoped>
</style>
