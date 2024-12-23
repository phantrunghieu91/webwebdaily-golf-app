<script lang="ts" setup>
import { ref } from 'vue';
import FeaturedItem from '@/components/FeaturedItem.vue';
const featuredItems = ref([
  {
    title: 'Alphabet pre-shot routine',
    isNew: true,
    postedAt: '4 mins',
  },
  {
    title: 'Relaxed concentration',
    isNew: false,
    postedAt: '3 mins',
  },
  {
    title: 'Stacking shots',
    isNew: false,
    postedAt: '1 day',
  },
]);
</script>
<template>
  <section class="py-8">
    <h2 class="text-3xl font-bold">Featured sessions</h2>
    <div class="flex gap-4 overflow-hidden mt-5">
      <FeaturedItem v-for="(item, index) in featuredItems" :key="index" :itemData="item" />
    </div>
  </section>
</template>