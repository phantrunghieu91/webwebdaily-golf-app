<script setup lang="ts">
import Header from '@/components/Header.vue';
import Nav from '@/components/Nav.vue';
import FeatureSessions from '@/components/FeatureSessions.vue';
import DiscoverSection from '@/components/DiscoverSection.vue';
</script>

<template>
  <div id="content" class="bg-gray-950 w-[26.875rem] mx-auto px-5 pt-10 pb-6 text-gray-200">
    <Header />
    <FeatureSessions />
    <DiscoverSection />
    <Nav />
  </div>
</template>