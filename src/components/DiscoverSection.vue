<script lang="ts" setup>
import DiscoverItem from './DiscoverItem.vue';
import { ref } from 'vue'
const discoverItems = ref([
  { title: 'Starter sessions', },
  { title: 'Mindful moments', },
  { title: 'On course', },
  { title: 'Home comfort', },
]);
</script>
<template>
  <section>
    <h2 class="text-3xl font-bold mb-5">Discover</h2>
    <div class="grid grid-cols-2 gap-3">
      <DiscoverItem v-for="(item, index) in discoverItems" :key="index" :itemData="item" />
    </div>
  </section>
</template>