<script lang="ts" setup>
import NavItem from '@/components/NavItem.vue';
import { ref } from 'vue';

const navItems = ref([
  { icon: 'mingcute:flag-3-line', text: 'Practice', active: true },
  { icon: 'mdi:book-open-page-variant', text: 'Journal', active: false },
  { icon: 'mdi:note-text', text: 'Notes', active: false },
  { icon: 'mdi:account', text: 'Profile', active: false },
]);

const handleChangeActiveItem = (index: number) => {
  navItems.value.forEach((item, i) => {
    item.active = i === index;
  });
}

</script>
<template>
  <nav class="py-4">
    <ul class="text-white flex justify-between text-sm">
      <NavItem v-for="(item, index) in navItems" :key="index" :index="index" :itemData="item" @handleClick="handleChangeActiveItem"/>
    </ul>
  </nav>
</template>