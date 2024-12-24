<script lang="ts" setup>
const props = defineProps<{
  itemData: {
    title: string;
  }
}>();
</script>
<template>
  <article class="flex items-center gap-3">
    <div class="w-16 aspect-square rounded-full bg-slate-700"></div>
    <h3>{{ props.itemData.title }}</h3>
  </article>
</template>