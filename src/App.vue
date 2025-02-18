<script setup lang="ts">
import BaseInfo from './components/BaseInfo.vue';
import FeatureSection from './components/FeatureSection.vue';
import ToursInfo from './components/ToursInfo.vue';
import Default from './layouts/default.vue';

</script>

<template>
    <Default>
        <main>
            <BaseInfo />
            <FeatureSection />
            <ToursInfo />
        </main>
    </Default>
</template>

<style scoped>
</style>
